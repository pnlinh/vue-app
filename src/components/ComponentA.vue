<template>
    <div class="hello">
        <h1>{{ message }}</h1>
        <p>Time now is: {{ currentDateTime }}</p>
        <p v-if="isShow">This line is hide/show</p>
        <ol>
            <li v-for="post in posts" v-bind:key="post.title">
                <p class="bold">{{ post.title }}</p>
                <p>{{ post.content }}</p>
            </li>
        </ol>
    </div>
</template>

<script>
    export default {
        name: 'ComponentA',
        props: {
            message: String
        },
        data() {
            return {
                currentDateTime: Date.now().toLocaleString(),
                isShow: true,
                posts: [
                    {
                        title: 'Why VueJs ?',
                        content: 'Vuejs is a frontend framework'
                    },
                    {
                        title: 'VueJs vs ReactJs ?',
                        content: 'Vuejs vs ReactJs are frontend framework'
                    },
                    {
                        title: 'VueJs call request to NodeJs',
                        content: 'Vuejs call api to NodeJs via axios, fetch'
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    h1 {
        color: red;
    }

    p.bold {
        font-weight: bold;
    }
</style>
