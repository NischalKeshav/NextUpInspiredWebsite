<script>
    let { event } = $props();
</script>

<div class="eventCard">
    <img src={event.image} alt={event.title} />
    <div class="content">
        <h3>{event.title}</h3>
        <p class="date">{event.date}</p>
        <p class="description">{event.description}</p>
    </div>
</div>

<style>
    .eventCard {
        position: relative;
        border-radius: 16px;
        border: 4px solid white;
        height: 70vh;
        width: 80vw;
        overflow: hidden;
    }
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .content {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        background: linear-gradient(to bottom, transparent 0%, rgba(0,0,0,0.7) 100%);
    }
    h3 {
        color: white;
        font-size: 2rem;
        font-weight: 600;
        margin: 0 0 0.5rem 0;
    }
    .date {
        color: white;
        font-size: 1.125rem;
        font-weight: 400;
        margin: 0 0 0.5rem 0;
    }
    .description {
        color: white;
        font-size: 1rem;
        font-weight: 300;
        margin: 0;
    }
</style>