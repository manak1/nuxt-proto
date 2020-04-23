<template>
  <section class="p-intro">
    <div class="p-intro__container">
      <div class="p-intro__profile">
        <h2 class="p-intro__name test">
          MANAKI<br />
          IKEDA
        </h2>
        <p class="p-intro__position test">
          Frontend Engineer.
        </p>
      </div>
      <div class="p-intro__hero">
        <kinesis-container class="p-intro__kinesis">
          <kinesis-element :strength="10" type="depth" class="p-intro__penguin">
            <img class="c-penguin" src="@/assets/image/penguin.svg" alt="" />
          </kinesis-element>
        </kinesis-container>
      </div>
    </div>
  </section>
</template>

<script>
import { KinesisElement, KinesisContainer } from 'vue-kinesis'
export default {
  components: {
    KinesisElement,
    KinesisContainer
  },
  mounted() {
    const tl = this.$gsap.timeline({
      repeat: 0,
      delay: 0.4
    })
    tl.to('.test', 1.3, { x: 0, ease: 'expor.in' }, 0)
    tl.to(
      '.c-penguin',
      0.4,
      { x: 200, opacity: 1, ease: 'expor.in', delay: 0.4 },
      0
    )
  }
}
</script>

<style lang="scss" scoped>
.p-intro {
  &__container {
    widows: 100%;
  }

  &__profile {
    position: absolute;
    top: 50%;
    left: 10%;
    transform: translateY(-50%);
    overflow: hidden;
  }

  &__name {
    @include text-white;
    font-size: 120px;
    line-height: 1;
    transform: translate(-1000px, 0px);
  }

  &__position {
    @include text-white;

    font-size: 28px;
  }

  &__hero {
    position: absolute;
    right: 0;
    left: 0;
    top: 10%;
    bottom: 0;
    height: 80vh;
  }

  &__kinesis {
    height: 80vh;
  }

  &__penguin {
    width: 500px;
    height: auto;
    margin-left: 40%;
  }
}

.c-penguin {
  transform: translate(500px, 0);
  opacity: 0;
}
</style>
