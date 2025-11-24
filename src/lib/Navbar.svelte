<script>
	import { Navlinks, Navlist } from '$lib/index.js';
	import logo from '$lib/assets/NU.png';
</script>
<nav>
	<img src={logo} alt="Logo" class="logo" />
	<ul>
		{#each Navlist as navItem, index}
			<li>
				<a href={Navlinks[index]}>{navItem}</a>
			</li>
		{/each}
	</ul>
	<button>Donate</button>
</nav>

<style>
	nav {
		display: flex;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		padding: 2rem 4rem;
		z-index: 1000;
		align-items: center;
		justify-content: space-between;
		background-color: white;
		padding: 0rem;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
	}

	.logo {
		height: 70px;
		width: auto;
	}

	ul {
		display: flex;
		gap: 2rem;
		width: 50%;
		list-style: none;
		margin: 0 auto;
		padding: 0;
		justify-content: center;
	}

	li {
		margin: 0;
		transition: color 0.3s;
	}

	a {
		color: black;
		text-decoration: none;
		padding: 0.5rem 1rem;
		border-radius: 4px;
		transition: background-color 0.3s;
		font-size: 1.125rem;
		font-weight: 500;
	}

	li:hover {
		color: #3388dd;
	}
	button {
		background-color: #3388dd;
		color: white;
		border: none;
		padding: 0.5rem 1rem;
		border-radius: 16px;
		transition: background-color 0.3s, transform 0.3s;
		font-size: 1.125rem;
		font-weight: 600;
		margin-right: 1rem;
	}
	button:hover {
		background-color: #2266aa;
		cursor: pointer;
		transform: rotateZ(360deg);
	}
	@media only screen and (max-width: 767px){
		nav {
			flex-direction: row;
		}
		ul {
			display: none;
		}
	}
</style>


