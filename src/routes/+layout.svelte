<script>
    import { onNavigate } from "$app/navigation";
    import { onMount } from "svelte";

    let scrollY = 0;

    onMount(() => {
        scrollY = window.scrollY;

        window.addEventListener('scroll', () => {
            scrollY = window.scrollY;
        });
    })

    // uncomment to delay navigation - shows flicker much more clearly
    // onNavigate(() => new Promise(res => setTimeout(res, 500)));
</script>

<div>Scroll Y: {scrollY}</div>

<slot></slot>


<style>
    div {
        background-color: black;
        color: white;
        position: fixed;
        bottom: 0;
        right: 0;
        padding: 1rem;
        font-size: 2rem;
    }
</style>