<template>
    <div class="admin-post-page">
        <section class="update-form">
            <AdminPostForm :post="loadedPost" />
        </section>
    </div>
</template>

<script>
    import AdminPostForm from "@/components/Admin/AdminPostForm";

    export default {
        layout: 'admin',
        components: {
            AdminPostForm
        },
        data() {
            return {
                loadedPost: {
                    author: 'Maximilian',
                    title: 'My awesome Post',
                    content: 'Super amazing thanks for that!',
                    thumbnailLink: 'https://st2.depositphotos.com/1297553/8277/v/600/depositphotos_82777500-stock-video-binary-digital-tech-data-code.jpg'
                }
            }
        }
    }
</script>

<style scoped>
    .update-form {
        width: 90%;
        margin: 20px auto;
    }
    @media (min-width: 768px) {
        .update-form {
            width: 500px;
        }
    }
</style>
