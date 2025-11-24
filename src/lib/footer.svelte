<div class="footer-wrapper">
    <hr class="footer-line" />
    <footer>
        <div class="footer-content">
            <p class="info1">Copyright © 2025 NextUp</p>
            <p class="info2">Website designed by <a href="https://github.com/NischalKeshav" target="_blank" rel="noopener noreferrer">Nischal Keshav</a></p>
        </div>
    </footer>
</div>

<style>
    .footer-wrapper {
        width: 100%;
        background-color: #1A345B;
    }

    .footer-line {
        border: none;
        border-top: 3px solid #3388dd;
        margin: 0;
        width: 100%;
    }

    footer {
        background-color: #1A345B;
        color: white;
        padding: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .footer-content {
        max-width: 1200px;
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        gap: 2rem;
    }

    .info1 {
        font-size: 1rem;
        font-weight: 400;
        color: white;
        margin: 0;
    }

    .info2 {
        font-size: 0.9rem;
        font-weight: 300;
        color: white;
        margin: 0;
    }

    a {
        color: white;
        text-decoration: underline;
        transition: color 0.3s ease;
    }

    a:hover {
        color: #3388dd;
    }

    @media only screen and (max-width: 767px) {
        footer {
            padding: 1.5rem;
        }

        .footer-content {
            flex-direction: column;
            align-items: flex-start;
            gap: 0.5rem;
        }

        .info1, .info2 {
            font-size: 0.875rem;
        }
    }
</style>