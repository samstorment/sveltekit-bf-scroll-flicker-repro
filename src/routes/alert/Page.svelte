<script>
    import { beforeNavigate } from "$app/navigation";
    
    export let slug;
    export let other;

    beforeNavigate(() => alert("BEFORE NAVIGATE"));
</script>


<h1>Page {slug}</h1>

<a href="https://github.com/sveltejs/kit">External Link</a>
<br>
<br>
<a href="/alert/{other}">Internal Link</a>
