<template>
        <div><strong>Название:</strong> {{ post.title }}</div>
       <div><strong>Описание:</strong> {{ post.body }}</div>
 <div class="post__btns">Delete</div>
</template>

<script>
    export default { 
        props: {
            post:{
                type: Object,
                reqiured: true,
            }
        }  
    }
</script>

<style scoped>
.post {
    padding: 15px;
    border: 1px solid teal;
    margin-top: 15px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>