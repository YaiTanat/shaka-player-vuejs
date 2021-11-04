<template>
  <div class="container">
    <video-player
      :license-server="licenseServer"
      :manifest-url="manifestUrl"
      :poster-url="posterUrl"
    />
  </div>
</template>

<script>
import VideoPlayer from '@/components/VideoPlayer.vue';

export default {
  components: { VideoPlayer },
  data() {
    return {
      licenseServer: 'https://widevine-proxy.appspot.com/proxy',
      manifestUrl:
        'https://dash.akamaized.net/dash264/TestCases/1c/qualcomm/2/MultiRate.mpd',
      posterUrl:
        'https://www.img.in.th/images/137e80e688d609c04d6c2cf8054f5eae.png'
    };
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.mx-auto {
  margin-left: auto;
  margin-right: auto;
}

.shadow-lg {
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1),
    0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.max-w-full {
  max-width: 100%;
}

.w-full {
  width: 100%;
}

.h-full {
  height: 100%;
}
</style>
