<script>
	import hero from '$lib/assets/hero.HEIC';
</script>

<div class="hero">
	<img src={hero} alt="Hero" class="hero-image" />
</div>

<style>
	.hero {
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.hero-image {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>