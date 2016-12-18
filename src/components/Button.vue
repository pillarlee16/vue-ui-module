<template>
<div class="button" v-on:mouseover="focusIn" v-on:mouseleave="focusOut">
  {{ value }}
</div>
</template>
<script>
import { TweenMax, Elastic, Expo } from 'gsap';

export default {
  data() {
    return {
      value: 'Click',
    };
  },
  methods: {
    focusIn() {
      const buttonEl = this.$el;
      TweenMax.to(buttonEl, 1.1, {
        scale: 1.25,
        ease: Elastic.easeOut,
        easeParams: [3, 2],
      });
    },
    focusOut() {
      const buttonEl = this.$el;
      TweenMax.to(buttonEl, 0.85, {
        scale: 1.0,
        ease: Expo.easeOut,
      });
    },
  },
};
</script>
<style>
.button {
  width: 200px;
  height: 60px;
  background-color: rgba(255, 255, 0, 1);
  border-radius: 3px;
  box-shadow: 2px 2px 2px 2px rgba(0, 0, 0, 0.1);
  text-align: center;
  line-height: 60px;
  font-weight: bold;
}

</style>
