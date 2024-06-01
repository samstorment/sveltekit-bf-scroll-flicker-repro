
<h1>How to Use</h1>

<ul>
    <li>Click "External Link" below which wll navigate you to an external site. Immediately navigate back using the browser back button</li>
    <li>Click "Internal Link" below which will take you to another page of this site. Scroll down a bit on the page (halfway is a good amount to make it clear), take note of the Scroll Y position, then back navigate</li>
    <li>Then just start alternating back and forward navigations between this page and the other page. (You can use <kbd>alt</kbd> + <kbd>right arrow</kbd> and <kbd>alt</kbd> + <kbd>left arrow</kbd> to do this quickly)</li>
</ul>

<p>
    <a href="https://github.com/sveltejs/kit">External Link</a>
</p>
<p>
    <a href="/flicker/2">Internal Link</a>
</p>

<h2>Note</h2>

<div class="note">
    <p>

        My expectation is that Scroll Y would just alternate back and forth as you switch between the two pages, but something causes the scroll Y positions to get out of whack. I think it could have something to do with the bfcache since I never have this issue on the dev server and bfcache is disabled there because there is a websocket connection for hot module reloading.
    </p>
    <p>
        I called this a "flicker" because I first noticed it when the scroll y position was causing the page to jump a bit too early before a navigation completed, but sometimes there's no visual flicker and the scroll y position still get messed up after back and forward navigations. The "flicker" seems to manifest more often on firefox but I've seen it on chrome too.
    </p>    
</div>



{#each { length: 100 } as _}
    <div style="padding: 1rem;">take up space to cause scroll</div>
{/each}


<style>
    ul {
        max-width: 40ch;
    }

    li {
        margin-bottom: 1rem;
    }

    .note {
        border: 1px solid;
        padding: 1rem;
        max-width: 80ch;
    }

    kbd {
        background-color: lightgray;
        box-shadow: 3px 3px 0px rgb(48, 48, 48);
        padding: .2rem;
        border-radius: .2rem;
    }
</style>