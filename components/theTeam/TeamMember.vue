<template>
    <div :class="$style.wrapper">
        <div style="height: 90px;"></div>
        <img :src="require(`@/assets/teams/${image}.png`)" alt="" width="100%">
        <div style="height: 15px;"></div>
        <p :class="$style.name">{{ name }}</p>
        <p :class="$style.name" style="font-weight: 200; font-size: 18px;">{{ role }}</p>
        <div :style="{height: gap}"></div>
        <p :class="$style.background">
            {{ bio }}
            <br><br>
            {{ email }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'TeamMember',
    props: {
        name: {
            type: String,
            required: true
        },
        bio: {
            type: String,
            required: true
        },
        image: {
            type: String,
            required: true
        },
        email: {
            type: String,
            required: true
        },
        role: {
            type: String,
            required: true
        },
        gap: {
            type: String,
            default: '90px'
        }
    }
}

</script>

<style lang="css" module>
.wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
}

.name {

    color: #282B46;
    text-align: justify;
    font-family: Spartan;
    font-size: 22px;
    font-style: normal;
    font-weight: 700;
    line-height: 33px; /* 150% */
    letter-spacing: 2.64px;
    text-align: center;
}

.background {
    color: #282B46;
    font-family: Spartan;
    font-size: 14px;
    font-style: normal;
    font-weight: 300;
    line-height: 22px; /* 157.143% */
}

img {
    border-radius: 50;
}
</style>