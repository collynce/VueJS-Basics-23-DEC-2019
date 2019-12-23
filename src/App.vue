<template>
    <div id="app">
        <Index/>
        <Data/>
    </div>
</template>

<script>
    import Index from './components/Index'
    import Data from './components/Data'
    export default {
        name: 'app',
        components: {
            Index,
            Data
        }
    }
</script>
<style lang="scss">
    /*#app {*/
    /*    font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
    /*    -webkit-font-smoothing: antialiased;*/
    /*    -moz-osx-font-smoothing: grayscale;*/
    /*    text-align: center;*/
    /*    color: #2c3e50;*/
    /*    list-style: none;*/
    /*}*/
</style>
