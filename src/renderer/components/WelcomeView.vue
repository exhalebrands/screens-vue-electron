<template>
  <v-layout>
    <v-scale-transition>
      <img :key="active" :src="`static/slide-${active}.jpg`" style="height: 100vh; width: 100%" alt="">
    </v-scale-transition>
  </v-layout>
</template>

<script>
export default {
  name: 'welcome',
  created: function () {
    var vm = this
    var activeIdx = 0
    setInterval(function () {
      activeIdx++
      if (activeIdx > 5) {
        activeIdx = 0
        vm.active = 0
      }
      vm.active = activeIdx
    }, 5000)
  },
  data () {
    return {
      active: 0,
      slides: [
        { id: 0, src: '/static/slide-0.jpg' },
        { id: 1, src: '/static/slide-1.jpg' },
        { id: 2, src: '/static/slide-2.jpg' },
        { id: 3, src: '/static/slide-3.jpg' },
        { id: 4, src: '/static/slide-4.jpg' },
        { id: 5, src: '/static/slide-5.jpg' },
        { id: 6, src: '/static/slide-6.jpg' },
        { id: 7, src: '/static/slide-7.jpg' },
        { id: 8, src: '/static/slide-8.jpg' },
        { id: 9, src: '/static/slide-9.jpg' },
        { id: 10, src: '/static/slide-10.jpg' },
        { id: 11, src: '/static/slide-11.jpg' },
        { id: 12, src: '/static/slide-12.jpg' },
        { id: 13, src: '/static/slide-13.jpg' },
        { id: 14, src: '/static/slide-14.jpg' },
        { id: 15, src: '/static/slide-15.jpg' },
        { id: 16, src: '/static/slide-16.jpg' },
        { id: 17, src: '/static/slide-17.jpg' },
        { id: 18, src: '/static/slide-18.jpg' },
        { id: 19, src: '/static/slide-19.jpg' },
        { id: 20, src: '/static/slide-20.jpg' },
        { id: 21, src: '/static/slide-21.jpg' },
        { id: 22, src: '/static/slide-22.jpg' },
        { id: 23, src: '/static/slide-23.jpg' },
        { id: 24, src: '/static/slide-24.jpg' },
        { id: 25, src: '/static/slide-25.jpg' },
        { id: 26, src: '/static/slide-26.jpg' },
        { id: 27, src: '/static/slide-27.jpg' },
        { id: 28, src: '/static/slide-28.jpg' },
        { id: 29, src: '/static/slide-29.jpg' },
        { id: 30, src: '/static/slide-30.jpg' },
        { id: 31, src: '/static/slide-31.jpg' },
        { id: 32, src: '/static/slide-32.jpg' },
        { id: 33, src: '/static/slide-33.jpg' }
      ]
    }
  }
}
</script>

<style scoped>
.centered {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
