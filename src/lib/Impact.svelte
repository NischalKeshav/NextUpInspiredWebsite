<script>
    import StudentsImpact from '$lib/studentsImpact.svelte';
    import Donations from '$lib/Donations.svelte';
    import Mentorsimpact from '$lib/Mentorsimpact.svelte';
    import BentImpact from '$lib/BentImpact.svelte';
</script>

<div class="impact">
    <h1>Our Impact</h1>
    <h2>Together, we're making a real difference in students' lives</h2>
    <div class="examples">
        <StudentsImpact></StudentsImpact>
        <Donations></Donations>
        <Mentorsimpact></Mentorsimpact>
        <BentImpact></BentImpact>
    </div>
</div>




<style>
    h1 {
        font-size: 4rem;
        font-weight: 600;
        text-align: center;
        margin-top: 2rem;
        color: #1A345B;
    }
    h2 {
        font-size: 2rem;
        font-weight: 300;
        text-align: center;
        margin-top: 1rem;
        color: #1A345B;
    }
    .impact {
        position: relative;


        justify-content: center;        width: 100%;
        background-color: #AAD2DA;
    }
    .examples {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 2rem;
        width: 100%;
        max-width: 1400px;
        margin: 0 auto;
        padding: 2rem;
    }

    @media only screen and (max-width: 767px) {
        .examples {
            grid-template-columns: 1fr;
            gap: 1rem;
        }
        h2 {
            display: none;
        }
    }
</style>