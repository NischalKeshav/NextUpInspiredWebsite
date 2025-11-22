<script>
    // @ts-nocheck
    import { onMount, onDestroy } from 'svelte';
    
    let num = $state(0);
    let finalNum = 400;
    let intervalId;
    let elementRef;
    let hasAnimated = false;

    function startCounter() {
        if (hasAnimated) return;
        hasAnimated = true;
        
        intervalId = setInterval(() => {
            num++;
            if (num >= finalNum) {
                num = finalNum;
                clearInterval(intervalId);
            }
        }, 800/finalNum);
    }

    onMount(() => {
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    startCounter();
                    observer.disconnect();
                }
            });
        }, {
            threshold: 0.5
        });

        if (elementRef) {
            observer.observe(elementRef);
        }

        return () => {
            observer.disconnect();
        };
    });

    onDestroy(() => {
        if (intervalId) {
            clearInterval(intervalId);
        }
    });
</script>

<div class="studentsImpact" bind:this={elementRef}>
    <h1>${num}+</h1>
    <h2>Donations and Sponsorships Earned</h2>
</div>


<style>
    .studentsImpact {
        position: relative;
        border-radius: 16px;
        border: 4px solid white;
        padding: 1rem;
        height: fit-content;
        width: 100%;
    }
    h1 {
        font-size: 2rem;
        font-weight: 600;
        color: #1A345B;
        text-align: center;
    }
    h2 {
        font-size: 1.5rem;
        font-weight: 300 ;
        color: #1A345B ;
        text-align: center;
    }
</style>