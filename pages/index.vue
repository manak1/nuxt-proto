<template>
  <no-ssr>
    <div v-if="loaded">
      <full-page id="fullpage" ref="fullpage" :options="options">
        <div class="section">
          <c-intro />
        </div>
        <div class="section">
          <h2>section2</h2>
        </div>
      </full-page>
    </div>
  </no-ssr>
</template>

<script>
import CIntro from '@/pages/-cIntro.vue'
export default {
  components: {
    CIntro
  },
  data() {
    return {
      options: {
        licenseKey: 'YOUR_KEY_HERE',
        menu: '#menu',
        anchors: ['page1', 'page2', 'page3'],
        easingcss3: 'cubic-bezier(0.25, 0, 0, 0.24)',
        afterLoad: this.afterLoad,
        animateAnchor: true,
        navigation: true,
        navigationPosition: 'left',
        onLeave: this.onMove
      },
      loaded: false
    }
  },
  mounted() {
    this.loaded = true
  },
  methods: {}
}
</script>
