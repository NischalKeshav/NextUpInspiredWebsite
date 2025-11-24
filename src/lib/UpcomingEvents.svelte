<script>
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
    let currentEvent = $state(0);
    let event = $state(events[currentEvent]);

    function nextEvent() {
        currentEvent++;
        event = events[currentEvent];
    }
    function previousEvent() {
        currentEvent--;
        event = events[currentEvent];
    }
</script>

<div class="upcomingEvents">
    <h2>Upcoming Events</h2>
</div>

<style>
    .upcomingEvents {
        position: relative;
    }
    h2 {
        font-size: 4rem;
        font-weight: 600;
        text-align: center;
        margin-top: 2rem;
        color: #1A345B;
    }
</style>