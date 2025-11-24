<script>
	import hero from '$lib/assets/hero.png';
</script>

<div class="hero">
	<img src={hero} alt="Hero" class="hero-image" />
	<div class="hero-text">
		<h1>The Future isn't Later</h1>
		<h1><i> it's Next Up</i></h1>
		<p>Mentoring middle school students to explore and discover their ideal career paths through interactive workshops, mentorship opportunities, and monthly career exploration events.</p>
	</div>
</div>

<style>
	.hero {
        position: relative;
        background-color: #1A345B;
        top: 0;
        left: 0;
        right: 0;
		display: flex;
		align-items: center;
        height: 90vh ;
		justify-content: center;
		overflow: hidden;
		width: 100%;
	}
	.hero::after {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(128, 128, 250, 0.5);
		pointer-events: none;
	}

	.hero-text {
		position: absolute;
		right: 4rem;
		top: 50%;
		transform: translateY(-50%);
		text-align: right;
		z-index: 10;
		color: white;
		text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
	}

	.hero-text h1 {
		font-size: 4rem;
		font-weight: 700;
		margin: 0;
		line-height: 1.2;
		color: white;
	}

	.hero-text h2 {
		font-size: 3rem;
		font-weight: 600;
		margin: 1rem 0 0 0;
		color: white;
	}

	.hero-image {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: left center;
	}
    @media only screen and (max-width: 767px){
        .hero {
            height: 80vh;
            background-color: #1A345B;
        }
       
        .hero::after {
            display: none;
        }
		p {
			display: none;
		}
        .hero-text {
            right: 2rem;
            left: 2rem;
            text-align: right;
            transform: translateY(-50%);
        }

        .hero-text h1 {
            font-size: 2.5rem;
        }

    } 
	.hero-text p {
		width: 50%;
		font-size: 1.5rem;
		font-weight: 300;
		color: white;
		text-align: right;
		margin: 1rem 0 0 auto;
		line-height: 1.2;
		text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.7);
	}
</style>