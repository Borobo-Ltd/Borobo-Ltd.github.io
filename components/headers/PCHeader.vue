
<template>
    <div v-show="showHeader" class="home_1_top" :style="{backgroundColor: scrollPosition > 0 ? stickyHeaderStyle.backgroundColor : null}">
        <div style="height: 65px;"></div>
        <nuxt-link v-if="scrollPosition > 0" to="/">
            <img v-if="isStickyHeaderDark" src="../../assets/logos/logo_white.svg" alt="" width="320px">
            <img v-else src="../../assets/logos/logo_black.svg" alt="" width="320px">
        </nuxt-link>
        <nuxt-link v-else to="/">
            <img v-if="isDark" src="../../assets/logos/logo_black.svg" alt="" width="320px">
            <img v-else src="../../assets/logos/logo_white.svg" alt="" width="320px">
        </nuxt-link>
        <div style="height: 35px;"></div>
        <ul class="navigation_bar">
            <li><NuxtLink to="/our-technology" :style="{color: getStickHeaderColor}">Our Technology</NuxtLink></li>
            <li><NuxtLink to="/design-center" :style="{color: getStickHeaderColor}">Design-Centred</NuxtLink></li>
            <li><NuxtLink to="/the-team" :style="{color: getStickHeaderColor}">The Team</NuxtLink></li>
            <li><NuxtLink to="/we-care" :style="{color: getStickHeaderColor}">Konpanion +</NuxtLink></li>
            <li><NuxtLink to="/kommunity" :style="{color: getStickHeaderColor}">Kommunity</NuxtLink></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'PCHeader',
    props: {
        isDark: {
            type: Boolean,
            default: false
        },
        isStickyHeaderDark: {
            type: Boolean,
            default: false
        },
    },
    data() {
        return {
            color: this.isDark ? '#282B46' : '#FFF',
            showHeader: true,
            scrollPosition: 0,
            stickyHeaderStyle: {
                backgroundColor: this.isStickyHeaderDark ? '#2F304D' : '#FDF9F3',
                color: this.isStickyHeaderDark ? '#FFF' : '#282B46'
            }

        }
    },
    computed: {
        getStickHeaderColor() {
            return this.scrollPosition > 0 ? this.stickyHeaderStyle.color : this.color;
        }
    },
    beforeDestroy() {
        window.removeEventListener('scroll', this.onScroll);
    },
    mounted() {
        window.addEventListener('scroll', this.onScroll);
    },
    methods: {
        onScroll() {
            const currentScrollPosition = window.scrollY;

            if (currentScrollPosition > this.scrollPosition) {
                this.showHeader = false;
            } else {
                this.showHeader = true;
            }


            this.scrollPosition = window.scrollY;



        }
    },
    // Your component's JavaScript logic goes here
}
</script>

<style scoped>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

ul {
    list-style: none;
}

a {
    text-decoration: none;
}

.home_1_top {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 50px;
    z-index: 100;
}

.navigation_bar {
    display: flex;
    justify-content: center;
    gap: 5vw;
}

.navigation_bar li a {
    padding: 10px;
    text-align: center;
    font-family: Spartan;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 25px; /* 156.25% */
    letter-spacing: 1.6px;
}
</style>