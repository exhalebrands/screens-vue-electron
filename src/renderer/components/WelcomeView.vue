<template>
  <v-layout>
    <v-scale-transition>
      <img :key="active" :src="`static/slide-${active}.jpg`" alt="">
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
          { id: 5, src: '/static/slide-5.jpg' }
        ]
      }
    }
  }
</script>

<style scoped>
  .centered
  {
    display: flex;
    justify-content: center;
    align-items: center;
  }

</style>
