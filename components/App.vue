<template>
    <div id="app" class="app">
        <header>
            <h1>Contained <code>position: fixed;</code></h1>
            <a href="https://github.com/arnellebalane/contained-position-fixed" target="_blank" rel="noopener noreferrer">
                github.com/arnellebalane/contained-position-fixed
            </a>
        </header>

        <main>
            <div class="container" :class="{contained}">
                <code><pre>.container {</pre></code>
                <code><pre>    width: 100%;</pre></code>
                <code><pre>    background-color: #3f51b5;</pre></code>
                <code>
                    <input type="checkbox" v-model="contained">
                    <pre>    contain: paint;</pre>
                </code>
                <code><pre>}</pre></code>

                <div class="element">
                    <code><pre>.element {</pre></code>
                    <code><pre>    width: 50vmin;</pre></code>
                    <code><pre>    height: 50vmin;</pre></code>
                    <code><pre>    position: fixed;</pre></code>
                    <code><pre>    right: 0;</pre></code>
                    <code><pre>    bottom: 0;</pre></code>
                    <code><pre>    background-color: #e91e63;</pre></code>
                    <code><pre>}</pre></code>
                </div>
            </div>
        </main>
    </div>
</template>

<script>
    export default {
        name: 'App',

        data() {
            return {
                contained: false
            };
        }
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
        color: #fff;
    }

    main code {
        position: relative;
        font-size: 20px;
    }

    main pre {
        margin: 0;
    }

    main input {
        position: absolute;
        top: 5px;
        left: 3ch;
        z-index: 1;
    }

    .container {
        width: 100%;
        background-color: #3f51b5;
    }

    .container.contained {
        contain: paint;
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
