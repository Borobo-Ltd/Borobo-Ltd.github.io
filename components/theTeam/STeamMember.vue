<template>
    <div :class="$style.wrapper">
        <div :style="{height: top}"></div>
        <img :src="require(`@/assets/teams/${image}.png`)" alt="" width="100%">
        <div style="height: 26px;"></div>
        <p :class="$style.name" :style="{fontSize: nameSize}">{{ name }}</p>
        <div style="height: 10px;"></div>
        <p :class="$style.name" :style="{ fontWeight: 200, fontSize: roleSize, lineHeight: roleHeight }">{{ role }}</p>
    </div>
</template>

<script>
export default {
    name: 'STeamMember',
    props: {
        name: {
            type: String,
            required: true
        },
        image: {
            type: String,
            required: true
        },
        role: {
            type: String,
            required: true
        },
        nameSize : {
            type: String,
            default: '22px'
        },
        roleSize : {
            type: String,
            default: '16px'
        },
        roleHeight: {
            type: String,
            default: '22px'
        },
        top: {
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
    font-size: 18px;
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