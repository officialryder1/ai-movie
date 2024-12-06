<script>
    import '../app.css'
    import "@fontsource/open-sans"
    let { children } = $props()
</script>

<main>
    {@render children()}
</main>
<footer>
    <p>made with 💖 by <a href="https://x.com/official_ryder0">official_ryder0</p>
</footer>
<style>
    :global(body){
        display: grid;
        grid-template-areas: "main main" "footer footer";
        min-height: 100vh;
        grid-template-columns: 1fr 300px;
        grid-template-rows:1fr auto;

    }
    main{
        
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 10px;
        grid-area: main;
    }
    footer{
        padding: 1em;
        color: #fff;
        background-color: #021526;
        grid-area: footer;
    }
    footer p {
        text-align: center;
        
    }
    a{
        text-decoration: none;
        font-weight: bold;
        color: #fff;
    }
</style>