<template>
    <div class="background-video">
        <video autoplay loop muted webkit-playsinline playsinline>
            <source :src="src" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</template>

<script>
export default {
    name: 'BackgroundVideo',
    props: {
        src: {
            type: String,
            required: true,
        },
    },
}
</script>

<style scoped>
.background-video {
    position: absolute;
    width: 100%;
    height: 100vh;
}

.background-video video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>