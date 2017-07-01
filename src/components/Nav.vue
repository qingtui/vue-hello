<template>
    <div class="nav">
        <h1>Navigation</h1>
        <ul>
            <li><router-link to="/hello">Vue Hello</router-link></li>
            <li><router-link to="/sass">Sass Hello</router-link></li>
            <li><router-link to="/element">Element Hello</router-link></li>
            <li><router-link to="/admin">Vue Element Admin</router-link></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'nav'
    }
</script>

<style scoped>
    .nav {
        padding: 10px;
    }

    h1, h2 {
        font-weight: normal;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        margin: 10px 0;
    }

    a {
        color: #42b983;
    }
</style>
