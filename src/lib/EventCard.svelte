<script>
    let { event, onNext } = $props();
</script>

<div class="eventCard">
    <img src={event.image} alt={event.title} />
    <button class="nextButton" onclick={onNext}>→</button>
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
        height: 70vh;
        width: 80vw;
        min-width: 80vw;
        overflow: hidden;
        flex-shrink: 0;
        margin-left: 3vw;
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
    .nextButton {
        position: absolute;
        top: 30vh;
        right: 2rem;
        z-index: 10;
        background-color: rgba(255, 255, 255, 0.9);
        color: #1A345B;
        border: none;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        font-size: 1.5rem;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: all 0.3s ease;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    .nextButton:hover {
        color: white;
        transform: scale(1.1);
    }
</style>