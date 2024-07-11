<template>
    <div :class="$style.carousel">
        <div :class="$style.carouselContainer">
            <div v-for="(item, index) in items" :key="index" :class="$style.carouselItem">
                <img :src="item.image" alt="">
                <p :class="$style.title">{{ item.title }}</p>
                <p :class="$style.description">{{ item.description }}</p>
            </div>
        </div>
    </div>
</template>



<script>
export default {
name: 'FlickitySlider',
components: {
},
data() {
    return {
    items: [
                {
                    title: 'MOOSKIT',
                    description: 'From the Shetland Islands',
                    image: require('@/assets/images/maah_chair_1.png')  // 경로 확인
                },
                {
                    title: 'SHOLMIT',
                    description: 'From the Shetland Islands',
                    image: require('@/assets/images/maah_chair_2.png')  // 경로 확인
                },
                {
                    title: 'EESIT',
                    description: 'From the Shetland Islands',
                    image: require('@/assets/images/maah_chair_3.png')  // 경로 확인
                },
            ]
    };
}
};
</script>

<style module>
.carousel {
    width: 100%;
    overflow: hidden;
    position: relative;
}

.carouselContainer {
    display: flex;
    animation: scroll 12s linear infinite;
}

.carouselItem {
    width: 290px; /* 아이템 너비를 290px로 설정 */
    flex-shrink: 0; /* 아이템이 축소되지 않도록 설정 */
    box-sizing: border-box;
    margin-right: 20px; /* 이미지 사이의 갭 추가 */
}

.carousel img {
    width: 100%;
    height: auto;
}

@keyframes scroll {
    0% {
        transform: translateX(0);
    }
    33.33% {
        transform: translateX(calc(-290px - 20px)); /* 첫 번째 아이템 너비 (290px) + 갭 (20px) */
    }
    66.66% {
        transform: translateX(calc((100% - 870px - 40px))); /* 두 번째 아이템 너비 (290px) + 갭 (20px) * 2 */
    }
    100% {
        transform: translateX(0); /* 처음 위치로 돌아가 반복 */
    }
}

.title {
    color: #000;
    font-family: Spartan;
    font-size: 16.258px;
    font-style: normal;
    font-weight: 300;
    line-height: 24.061px; /* 148% */
    padding-top: 25px;
}

.description {
    color: #000;
    font-family: Spartan;
    font-size: 13.006px;
    font-style: normal;
    font-weight: 300;
    line-height: 24.061px; /* 185% */
}
</style>









