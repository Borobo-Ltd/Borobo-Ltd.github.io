<script setup>
import { ref, onMounted } from '@nuxtjs/composition-api';

const posts = ref([]);

onMounted(() => {
    fetch('http://localhost:1337/api/posts?populate=*')
        .then(response => response.json())
        .then(data => {
            // 로그로 데이터 구조 확인
            console.log(data);

            // 데이터 구조화
            if (Array.isArray(data.data)) {
                posts.value = data.data.map(post => ({
                    id: post.id,
                    title: post.attributes.title,
                    description: post.attributes.description,
                    image: post.attributes.image ? post.attributes.image.data : []
                }));
            } else {
                console.error('Expected data.data to be an array');
            }

            // 로그로 구조화된 데이터 확인
            console.log(posts.value);
        });
});
</script>

<template>
    <div>
        <div v-for="post in posts" :key="post.id">
            <h2>{{ post.title }}</h2>
            <p>{{ post.description }}</p>
            <div v-if="post.image">
                <div v-for="image in post.image" :key="image.id">
                    <img :src="`http://localhost:1337${image.attributes.url}`" alt="Image">
                </div>
            </div>
        </div>
    </div>
</template>
