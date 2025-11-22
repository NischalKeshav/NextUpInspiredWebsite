<script>
	import hero from '$lib/assets/hero.png';
</script>

<div class="hero">
	<img src={hero} alt="Hero" class="hero-image" />
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
		content: '<h1>Hello</h1>';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(128, 128, 250, 0.5);
		pointer-events: none;

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
    } 
</style>