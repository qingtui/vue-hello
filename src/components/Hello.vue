<template>
    <div class="hello">
        <h3><router-link to="/">go back to Nav</router-link></h3>
        <h1>Vue Hello</h1>
        <h2>{ { message } }</h2>
        <div>{{ message }}</div>
        <h2>v-text</h2>
        <div><span v-text="message"></span></div>
        <h2>v-html</h2>
        <div v-html="message"></div>
        <h2>v-show</h2>
        <button v-on:click="show=!show">show / hide</button>
        <div v-show="show">{{ message }}</div>
        <h2>v-if</h2>
        <button v-on:click="show=!show">toggle</button>
        <div v-if="show">{{ message }}</div>
        <h2>v-else</h2>
        <button v-on:click="show=!show">toggle</button>
        <div v-if="show">if message</div>
        <div v-else>else message</div>
        <h2>v-else-if</h2>
        <button v-on:click="num=num==2?0:++num">toggle</button>
        <div v-if="num==0">if</div>
        <div v-else-if="num==1">else if</div>
        <div v-else>else</div>
        <h2>v-for</h2>
        <div><ul><li v-for="str in array">{{ str }}</li></ul></div>
        <h2>v-on[@]</h2>
        <div><button v-on:click="message=message=='Hello Vue!'?'Vue Hello!':'Hello Vue!'">v-on:click</button></div>
        <div><button @click="reverse">@click</button></div>
        <h2>v-bind[:]</h2>
        <div><span v-bind:title="message">{{ message }}</span></div>
        <div><span :title="message">{{ message }}</span></div>
    </div>
</template>

<script>
    export default {
        name: 'hello',
        data () {
            return {
                message: 'Hello Vue!',
                show: true,
                num: 0,
                array: ['one', 'two', 'three']
            }
        },
        methods: {
            reverse() {
                this.message = this.message==='Hello Vue!'?'Vue Hello!':'Hello Vue!'
            }
        }
    }
</script>

<style scoped>
    .hello {
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
