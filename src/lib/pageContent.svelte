<script>
    import logo from '../assets/svelte.png'
    import Counter from './Counter.svelte'

    export let pageNumber

    const switchPage = ()=>(pageNumber ^= 1)
</script>

<div class="main">
    <div>
        <h1>Page #{pageNumber}</h1>
        <button on:click={switchPage} class="h1">Switch page</button>
        <button on:click={() => window.print()} class="h1">Print page</button>
    </div>

    <img src={logo} alt="Svelte Logo"/>
    <h1>Hello world!</h1>

    <Counter/>

    <p>
        Visit <a href="https://svelte.dev">svelte.dev</a> to learn how to build Svelte
        apps.
    </p>

    <p>
        Check out <a href="https://github.com/sveltejs/kit#readme">SvelteKit</a> for
        the officially supported framework, also powered by Vite!
    </p>
</div>

<style>
    button {
        border-radius: 0.2em;
    }
</style>
