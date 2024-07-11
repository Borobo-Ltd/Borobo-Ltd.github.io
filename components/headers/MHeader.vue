<template>
    <div class="header">
        <div class="sized_box"></div>
        <nuxt-link v-if="isLogo" to="/">
            <img v-if="isDark" src="../../assets/logos/logo_black.svg" alt="">
            <img v-else src="../../assets/logos/logo_white.svg" alt="">
        </nuxt-link>
        <div class="burger" @click="toggleMenu">
            <div :style="{background: color}"></div>
            <div :style="{background: color}"></div>
            <div :style="{background: color}"></div>
        </div>
        <div v-if="isShowing" class="menu_container">
            <div class="close_container" @click="onClose">
                <div class="close"></div>
            </div>
            <ul>
                <li v-for="route in routes" :key="route.name">
                    <nuxt-link :to="route.link" :class="isSelected(route.link) ? 'selected_font' : 'unselected_font'">{{ route.name }}</nuxt-link>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import { ref, useRoute, computed } from '@nuxtjs/composition-api';

export default {
    name: 'MHeader',
    props: {
        isLogo: {
            type: Boolean,
            default: true
        },
        isDark: {
            type: Boolean,
            default: true
        }
    },
    setup() {
        const isShowing = ref(false);
        const route = useRoute();

        const currentPath = computed(() => route.value.path);

        return { isShowing, currentPath }
    },
    data() {
        return {
            color: this.isDark ? '#282B46' : '#FFF',
            routes: [
                { name: 'HOME', link: '/' },
                { name: 'OUR TECHNOLOGY', link: '/our-technology' },
                { name: 'DESIGN-CENTRED', link: '/design-center' },
                { name: 'THE TEAM', link: '/the-team' },
                { name: 'KONPANION +', link: '/we-care' },
                { name: 'KOMMUNITY', link: '/kommunity' }
            ],
            selectedStyle: {
            }
        }
    },
    methods: {
        toggleMenu() {
            this.isShowing = !this.isShowing;
            console.log(this.isShowing);
        },
        isSelected(link) {
            return this.currentPath === link;
        },
        onClose() {
            this.isShowing = false;
        }
    }
}
</script>

<style lang="css" scoped>
    .header {
        width: 100vw;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 40px 5%;
    }

    .sized_box {
        width: 30px;
        height: 30px;
    }

    .burger {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        width: 30px;
        height: 30px;
        cursor: pointer;
    }

    .burger * {
        width: 100%;
        height: 2.5px;
    }

    .close:after {
        display: inline-block;
        content: "\00d7";
        font-size: 40px;
        font-weight: 200;
        color: #282B46;
    }
    
    .close_container {
        display: flex;
        justify-content: flex-end;
        padding: 5%;
        cursor: pointer;
    }

    .menu_container {
        position: fixed;
        display: flex;
        flex-direction: column;
        top: 0;
        right: 0;
        width: 100vw;
        height: 100dvh;
        background: #FDF9F3;
        z-index: 100;
    }

    .selected_font {
        color: #282B46;
        text-align: center;
        font-family: Spartan;
        font-size: 25px;
        font-style: normal;
        font-weight: 500;
        line-height: 112.078%; /* 28.02px */
        letter-spacing: 2.5px;
    }

    .unselected_font {
        color: rgba(40, 43, 70, 0.6);
        text-align: center;
        font-family: Spartan;
        font-size: 25px;
        font-style: normal;
        font-weight: 300;
        line-height: 112.078%; /* 28.02px */
        letter-spacing: 2.5px;
    }

    ul {
        list-style: none;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        height: 100%;
        
    }

    li {
        display: flex;
        justify-content: center;
    }

    a {
        text-decoration: none;
    }
</style>