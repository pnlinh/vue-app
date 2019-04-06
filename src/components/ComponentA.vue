<template>
    <div class="hello">
        <h1>{{ message }}</h1>
        <p>Time now is: {{ currentDateTime }}</p>
        <p v-if="isShow">This line is hide/show</p>

        <label>
            <input type="text" v-model="newPost.title" placeholder="Title...">
        </label>
        <p>{{ this.newPost.title }}</p>
        <label>
            <input type="text" v-model="newPost.content" placeholder="Content...">
        </label>
        <p>{{ this.newPost.content }}</p>
        <button v-on:click="addPost">Add post</button>

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
                ],
                newPost: {title: '', content: ''}
            }
        },
        methods: {
            addPost() {
                this.posts.unshift(this.newPost);
                this.newPost = {title: '', content: ''}
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
