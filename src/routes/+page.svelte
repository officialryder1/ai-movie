<script>
    import ThemeToggle from "$lib/components/ThemeToggle.svelte";
    import MovieCard from "$lib/components/MovieCard.svelte";

    let show = false
</script>

<ThemeToggle/>
<h1>AI Movie Suggester</h1>
<div class="typing-container">
    <p class="typing-animation">
        we suggest a similar movie to your input.
    </p>
</div>
<form>
    <input type="text" placeholder="movie name">
    <button onclick={show = !show}>search</button>
</form>
<div>
    {#if show}
        <h1>Results</h1><br>
        <MovieCard/>
    {/if}
</div>

<style>
    h1{
        letter-spacing: 2px;
        font-weight: bolder;
        line-height: -1;
    }
    form input {
        width: 250px;
        height: 35px;
        border-radius: 5px;
        text-align: center;
        border: none;
        box-shadow: 2px 8px rgba(0,0,0,0.3);
        margin-right: 10px;
        transition: box-shadow 0.5s ease, border-top 0.5s ease-in-out;
    }
    input:focus{
        outline: none;
        box-shadow: 4px 9px rgba(0, 0, 0, 0.5);
        border-right: 1px solid orangered;
        border-top: 1px solid orangered;
    }
    button {
      width: 55px;
      height: 43px;
      border-radius: 5px;
      border: none;
      box-shadow: 4px 8px rgba(0, 0, 0, 0.3);
      font-weight: 600;
      letter-spacing: 1px;
      cursor: pointer;
    }
    .typing-container{
        display: inline-block;
        overflow: hidden;
        white-space: nowrap;
        border-right: 2px solid orangered;
        animation: typing 5s steps(60, end), blink 0.6s step-end infinite;
    }
    .typing-animation{
        color: #021526;
        transition: animation 2s ease-in-out;
        letter-spacing: 2px;
    }

    @keyframes typing{
        from {
            width: 0;
        }
        to {
            width: 45%;
        }
    }

    @keyframes blink {
        from, to {
            border-color: transparent;
        }
        50% {
            border-color: orangered ;
        }
    }
</style>