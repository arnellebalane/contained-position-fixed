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
                <div class="element"></div>
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

    .container {
        width: 100%;
        background-color: #3F51B5;
    }

    .element {
        width: 50vw;
        height: 50vh;
        position: fixed;
        right: 0;
        bottom: 0;
        background-color: #E91E63;
    }
</style>
