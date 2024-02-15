<script>
    import { onNavigate } from "$app/navigation";

    // uncomment to delay navigation - shows flicker much more clearly
    // onNavigate(() => new Promise(res => setTimeout(res, 500)));
</script>

<slot />