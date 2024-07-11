<template>
    <div class="video-container">
      <video-player
        ref="videoPlayer"
        class="video-js "
        :style="{height: height, minWidth: width}"
        :options="videoOptions"
      ></video-player>
    </div>
  </template>
        <!-- @ready="onPlayerReady" -->
  
  <script>
  export default {
    props: {
      height: {
        type: String,
        default: '100vh',
      },
      width: {
        type: String,
        default: '100%',
      },
    },
    data() {
      return {
        videoOptions: {
          autoplay: true,
          controls: false, // 조작 버튼을 숨기기 위해 controls를 false로 설정
          muted: true,
          loop: true,
          sources: [
            {
              src: '/videos/maah_video_1.mp4', // 낮은 화질의 비디오 소스
              type: 'video/mp4',
            },
          ],
          controlBar: {
            volumePanel: false,
            fullscreenToggle: false,
          },
          fluid: true,
        },
      };
    },
    mounted() {
      // this.onPlayerReady(this.$refs.videoPlayer.player);
    },
    methods: {
      onPlayerReady(player) {
        // 고화질 비디오의 소스
        const highQualitySource = {
          src: '/videos/maah_video_1_high.mp4',
          type: 'video/mp4',
        };
  
        // 임시 비디오 엘리먼트 생성
        const tempVideo = document.createElement('video');
        tempVideo.src = highQualitySource.src;
  
        // 고화질 비디오가 완전히 로드되면 소스 대체
        tempVideo.addEventListener('canplaythrough', () => {
          player.src([highQualitySource]);
          player.play();
        });
  
        // 임시 비디오 로드 시작
        tempVideo.load();
      },
    },
  };
  </script>
  
  <style scoped>
  @import 'video.js/dist/video-js.css';



  .video-container {
    width: 100%;
    height: 100vh;
    position: relative;
    overflow: hidden;
}

.video-js {
    width: 100% !important;
    height: 100% !important;
    object-fit: cover;
}


  </style>
  