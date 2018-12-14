<template>
  <div class="flex flex-row items-center border-b border-l border-r p-6 cursor-pointer" @click="startVideo">
    <div class="flex-initial w-32 h-18 mr-6">
      <div class="coverWrapper">
        <div class="cover" :class="cover"></div>
      </div>
    </div>
    <div class="flex-1">
      <div class="">第{{ number }}集</div>
      <div class="text-grey text-sm">{{ duration }}</div>
    </div>
    <div class="flex-initial text-green hover:text-green-dark">
      <i class="far fa-play-circle fa-2x"></i>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'video-item',
    props: ['number', 'duration', 'video'],
    data: function() {
      return {
        cover: 'cover--video' + this.number
      }
    },
    methods: {
      startVideo: function() {
        this.$parent.modal = true
        this.$parent.episode = this.number
        this.$parent.video = this.video
        // this.$parent.cover = this.cover
      }
    }
  }
</script>