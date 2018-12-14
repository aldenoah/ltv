<template>
  <section>
    <div class="container mx-auto cover--poster bg-black">
      <div class="p-6">
        <div class="my-8">
          <h1 class="text-white">Kill Me Heal Me 杀了我治愈我</h1>
          <div class="text-white">讲述有七重人格的财阀三世和他的秘密女主治医生——专修一年的实习女医师的治愈系、搞笑、浪漫、爱情故事
          </div>
        </div>
      </div>
    </div>

    <div class="container mx-auto">
      <video-item number='1' duration='61:41' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24767.html"></iframe>'></video-item>

      <video-item number='2' duration='61:34' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24768.html"></iframe>'></video-item>

      <video-item number='3' duration='61:03' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24769.html"></iframe>'></video-item>

      <video-item number='4' duration='61:39' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24770.html"></iframe>'></video-item>

      <video-item number='5' duration='61:13' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24771.html"></iframe>'></video-item>

      <video-item number='6' duration='61:45' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24772.html"></iframe>'></video-item>

      <video-item number='7' duration='63:00' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24773.html"></iframe>'></video-item>

      <video-item number='8' duration='62:19' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24774.html"></iframe>'></video-item>

      <video-item number='9' duration='62:32' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24775.html"></iframe>'></video-item>

      <video-item number='10' duration='61:42' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24776.html"></iframe>'></video-item>

      <video-item number='11' duration='62:01' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24777.html"></iframe>'></video-item>

      <video-item number='12' duration='62:43' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24778.html"></iframe>'></video-item>

      <video-item number='13' duration='62:19' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24779.html"></iframe>'></video-item>

      <video-item number='14' duration='60:58' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24780.html"></iframe>'></video-item>

      <video-item number='15' duration='61:41' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24781.html"></iframe>'></video-item>

      <video-item number='16' duration='61:18' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24782.html"></iframe>'></video-item>

      <video-item number='17' duration='60:25' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24783.html"></iframe>'></video-item>

      <video-item number='18' duration='61:08' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24784.html"></iframe>'></video-item>

      <video-item number='19' duration='58:17' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24785.html"></iframe>'></video-item>

      <video-item number='20' duration='60:17' video='<iframe width="100%" height="100%" src="https://www.hanjutv.com/player/24786.html"></iframe>'></video-item>

    </div>

    <div id="myModal" class="modal bg-black" v-show="modal">
      <div class="modal-content bg-black text-white">
        <div class="flex items-center m-6">
          <div class="flex-1 close" @click="closeModal">
            <i class="fas fa-arrow-left"></i>
          </div>
          <div class="flex-initial">第{{ episode }}集</div>
        </div>
        <div class="videoWrapper" :class="cover" v-html="video"></div>
      </div>
    </div>
  </section>
</template>

<script>
import VideoItem from '~/components/VideoItem.vue'

export default {
  components: {
    VideoItem
  },
  data: function() {
    return {
      menu: false,
      modal: false,
      episode: null,
      video: null,
      cover: null
    }
  },
  methods: {
    closeMenu: function() {
      this.menu = false
    },
    closeModal: function() {
      this.modal = false
      this.video = null
    }
  }
}
</script>

