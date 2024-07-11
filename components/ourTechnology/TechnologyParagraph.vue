<template>
    <div style="padding: 0 10%;">
        <pre class="title" :style="{ color: color, textAlign: textAlign }">{{ title }}</pre>
        <p class="description" :style="{ color: color }">{{ description }}</p>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        color: {
            type: String,
            required: true
        },
        textAlign: {
            type: String,
            default: 'left'
        }
    }
}
</script>

<style lang="css" scoped>
    .title {
        font-family: Spartan;
        font-size: 34px;
        font-style: normal;
        font-weight: 500;
        line-height: 37px; /* 108.824% */
    }

    .description {
        padding-top: 30px;
        font-family: Spartan;
        font-size: 17px;
        font-style: normal;
        font-weight: 250;
        line-height: 22.876px; /* 134.563% */
    }
</style>