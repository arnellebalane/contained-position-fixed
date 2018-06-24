<template>
    <div id="app" class="app">
        <header>
            <h1>Contained <code>position: fixed;</code></h1>
            <a href="https://github.com/arnellebalane/contained-position-fixed" target="_blank" rel="noopener noreferrer">
                github.com/arnellebalane/contained-position-fixed
            </a>
        </header>

        <main>
            <div class="container">
                <pre><code>.container {</code></pre>
                <pre><code>    width: 100%;</code></pre>
                <pre><code>    background-color: #3f51b5;</code></pre>
                <pre><code>    contain: paint;</code></pre>
                <pre><code>}</code></pre>

                <div class="element">
                    <pre><code>.element {</code></pre>
                    <pre><code>    width: 50vmin;</code></pre>
                    <pre><code>    height: 50vmin;</code></pre>
                    <pre><code>    position: fixed;</code></pre>
                    <pre><code>    right: 0;</code></pre>
                    <pre><code>    bottom: 0;</code></pre>
                    <pre><code>    background-color: #e91e63;</code></pre>
                    <pre><code>}</code></pre>
                </div>
            </div>
        </main>
    </div>
</template>

<script>
    export default {
        name: 'App'
    };
</script>

<style scoped>
    .app {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    header {
        flex-shrink: 0;
        padding: 52px 10vmin;
        text-align: center;
    }

    main {
        flex-grow: 1;
        display: flex;
        padding: 10vmin;
        padding-top: 0;
    }

    main div {
        padding: 5vmin;
    }

    main pre {
        margin: 0;
    }

    main code {
        display: block;
        color: #fff;
    }

    .container {
        width: 100%;
        background-color: #3f51b5;
    }

    .element {
        width: 50vw;
        height: 50vh;
        position: fixed;
        right: 0;
        bottom: 0;
        background-color: #e91e63;
    }
</style>
