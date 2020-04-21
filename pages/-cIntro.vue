<template>
  <section class="p-intro">
    <div class="p-intro__container">
      <div class="p-intro__profile">
        <h2 class="p-intro__name">
          MANAKI<br />
          IKEDA
        </h2>
        <p class="p-intro__position">
          Frontend Engineer.
        </p>
      </div>
      <div class="p-intro__hero">
        <kinesis-container class="p-intro__kinesis">
          <kinesis-element :strength="10" type="depth" class="p-intro__penguin">
            <img src="@/assets/image/logo.svg" alt="" />
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
  }

  &__name {
    @include text-white;
    font-size: 120px;
    line-height: 1;
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
</style>
