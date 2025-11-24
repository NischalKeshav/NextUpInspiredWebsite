<script>
    import BHStigers from '$lib/assets/BHStigers.png';
    import bizzybbakers from '$lib/assets/bizzybbakery.webp';
    import BPL from '$lib/assets/BPL.png';
    import cloud4kids from '$lib/assets/cloud4.png';
    import elev8 from '$lib/assets/elev8.png';
    import GenerationsBank from '$lib/assets/GenerationsBank.png';
    import ziggys from '$lib/assets/ziggis.png';

    let sponsors = [
        { name: 'BH Tigers', image: BHStigers },
        { name: 'Bizzy B Bakery', image: bizzybbakers },
        { name: 'Bentonville Public Library', image: BPL },
        { name: 'Cloud 4 Kids', image: cloud4kids },
        { name: 'Elev8', image: elev8 },
        { name: 'Generations Bank', image: GenerationsBank },
        { name: "Ziggy's Pizza", image: ziggys }
    ];
</script>

<div class="sponsors">
    <h1>Our Sponsors</h1>
    <div class="carousel-container">
        <div class="sponsors-track">
            {#each sponsors as sponsor}
                <div class="sponsor-item">
                    <img src={sponsor.image} alt={sponsor.name} />
                </div>
            {/each}
            {#each sponsors as sponsor}
                <div class="sponsor-item">
                    <img src={sponsor.image} alt={sponsor.name} />
                </div>
            {/each}
        </div>
    </div>
</div>

<style>
    .sponsors {
        color: #1A345B;
        min-height: 50vh;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 4rem 0;
        background-color: #f5f5f5;
        overflow: hidden;
    }
    
    h1 {
        font-size: 4rem;
        font-weight: 600;
        text-align: center;
        margin-bottom: 4rem;
        color: #1A345B;
    }
    
    .carousel-container {
        overflow: hidden;
        width: 100%;
        position: relative;
        padding: 2rem 0;
    }
    
    .sponsors-track {
        display: flex;
        flex-direction: row;
        gap: 4rem;
        animation: scroll 30s linear infinite;
        width: fit-content;
    }
    
    .sponsors-track:hover {
        animation-play-state: paused;
    }
    
    @keyframes scroll {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(-50%);
        }
    }
    
    .sponsor-item {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 2rem 3rem;
        background: white;
        border-radius: 16px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        min-width: 250px;
        height: 180px;
        flex-shrink: 0;
    }
    
    .sponsor-item img {
        max-width: 200px;
        max-height: 140px;
        width: auto;
        height: auto;
        object-fit: contain;
    }
    
    @media only screen and (max-width: 767px) {
        h1 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }
        
        .sponsors-track {
            gap: 2rem;
            animation: scroll 20s linear infinite;
        }
        
        .sponsor-item {
            padding: 1.5rem 2rem;
            min-width: 200px;
            height: 140px;
        }
        
        .sponsor-item img {
            max-width: 150px;
            max-height: 100px;
        }
    }
</style>