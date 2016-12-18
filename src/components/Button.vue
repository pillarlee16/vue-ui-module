<template>
<div class="button">
  {{ value }}
</div>
</template>
<script>
export default {
  data() {
    return {
      value: 'Click',
    };
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
