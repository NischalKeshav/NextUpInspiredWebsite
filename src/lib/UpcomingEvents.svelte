<script>
    // @ts-nocheck
    import EventCard from '$lib/EventCard.svelte';

    import img1 from '$lib/assets/stemactivities.jpg';
    import img2 from '$lib/assets/stemactivities2.jpg';
    import img3 from '$lib/assets/stemactivities3.jpg';
    let events = [
        {
            title: 'Event 1',
            date: '2025-01-01',
            description: 'Description 1',
            image: img1
        },
        {
            title: 'Event 2',
            date: '2025-01-02',
            description: 'Description 2',
            image: img2
        },
        {
            title: 'Event 3',
            date: '2025-01-03',
            description: 'Description 3',
            image: img3
        }
    ]
    let numEvents = $state(events.length);
    let currentEvent = $state(0);
    let translateX = $state(0);
    let isAnimating = $state(false);
    let disableTransition = $state(false);

    function getEvent(offset) {
        return events[(currentEvent + offset + numEvents) % numEvents];
    }

    const pushEvent = () => {
        if (isAnimating) return;
        isAnimating = true;
        disableTransition = false;
        
        // Start the slide animation
        translateX = -1;
        
        setTimeout(() => {
            // First, disable transition
            disableTransition = true;
            
            // Wait for the browser to apply the transition disable
            requestAnimationFrame(() => {
                // Now update position and content
                currentEvent = (currentEvent + 1) % numEvents;
                translateX = 0;
                
                // Wait another frame before re-enabling transitions
                requestAnimationFrame(() => {
                    disableTransition = false;
                    isAnimating = false;
                });
            });
        }, 600);
    }
</script>
<h1>Upcoming Events</h1>
<div class="upcomingEvents">
    <div class="cards-container" style="transform: translateX(calc({translateX} * (80vw + 2rem))); transition: {disableTransition ? 'none' : 'transform 0.6s ease-in-out'}">
        <EventCard event={getEvent(0)} onNext={pushEvent} />
        <EventCard event={getEvent(1)} onNext={pushEvent} />
        <EventCard event={getEvent(2)} onNext={pushEvent} />
    </div>
</div>
<style>
    .upcomingEvents {
        position: relative;
        overflow-x: hidden;
        overflow-y: hidden;
        padding: 2rem 0;
    }
    
    .cards-container {
        display: flex;
        flex-direction: row;
        gap: 2rem;
    }
    
    h1 {
        font-size: 4rem;
        font-weight: 600;
        text-align: center;
        margin-top: 2rem;
        color: #1A345B;
    }

</style>