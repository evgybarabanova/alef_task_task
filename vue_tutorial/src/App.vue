<template>
<post-form @create="createPost"/>
<post-list :posts="posts"/>
</template>
    
<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
                { id: 1, title: 'Js 1', body: 'description 1' },
                { id: 2, title: 'Js 2', body: 'description 2' },
                { id: 3, title: 'Js 3', body: 'description 3' }
            ]
        }
    },
    methods: {
        createPost(post) {
    this.posts.push(post);
        }
    }
}
</script>
    
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>


<!-- 50 -->