<template>
    <div class="wrapper">
        <div style="height: 36px"></div>
        <img :src="require(`@/assets/images/${image}.png`)" alt="" />
        <div style="height: 36px"></div>
        <p class="name">{{ name }}</p>
        <div style="height: 36px"></div>
        <p class="description">{{ description }}</p>
    </div>
</template>

<script>
export default {
    name: 'MHomeItem',
    props: {
        name: {
            type: String,
            default: ''
        },
        description: {
            type: String,
            default: ''
        },
        image: {
            type: String,
            default: ''
        },
    }
}
</script>

<style scoped>
.wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.name {
    color: #282B46;
    font-family: Spartan;
    font-size: 17px;
    font-style: normal;
    font-weight: 600;
    line-height: 17px; /* 100% */
    text-align: left;
    letter-spacing: 0.85px;
}

.description {
    color: #282B46;
    text-align: justify;
    font-family: Spartan;
    font-size: 13px;
    font-style: normal;
    font-weight: 300;
    line-height: 18px; /* 138.462% */
    letter-spacing: 0.65px;
}
</style>