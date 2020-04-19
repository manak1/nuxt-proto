<template>
  <no-ssr>
    <div>
      <full-page id="fullpage" ref="fullpage" :options="options">
        <div class="section">
          <kinesis-container>
            <h2>section1</h2>
            <button class="next" @click="$refs.fullpage.api.moveSectionDown()">
              Next
            </button>
            <kinesis-element :strength="20" type="depth">
              <img
                src="@/assets/image/logo.svg"
                style="width:500px; height:auto; margin-left:40%;"
                alt=""
              />
            </kinesis-element>
          </kinesis-container>
        </div>
        <div class="section">
          <h2>section2</h2>
        </div>
      </full-page>
    </div>
  </no-ssr>
</template>

<script>
import { KinesisContainer, KinesisElement } from 'vue-kinesis'
export default {
  components: {
    KinesisContainer,
    KinesisElement
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
        navigationPosition: 'left'
      },
      show: false
    }
  },
  mounted() {
    setTimeout(() => {
      this.show = true
    }, 500)
  },
  methods: {
    afterLoad() {}
  }
}
</script>
