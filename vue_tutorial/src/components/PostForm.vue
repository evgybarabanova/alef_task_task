<template>
    <form>
        <h4>Create post</h4>
        <input v-model="post.title" class="input" type="text" placeholder="name of post ">
        <input v-model="post.body" class="input" type="text" placeholder="description">
        <button @click="createPost">create</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now(),
            this.$emit('create', this.post)
            this.post= {
                title: '',
                body: '',    
            }
        }
    }
}
</script>

<style scoped>
.input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
}

form {
    display: flex;
    flex-direction: column;
}

form button {
    align-self: flex-end;
    margin-top: 15px;
    padding: 10px 15px;
    background-color: transparent;
    color: teal;
    border: 1px solid teal;
}
</style>