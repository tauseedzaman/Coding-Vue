<template>
  <button @click="increaseCounter">{{ state.count }}</button>
</template>
<script>
import { reactive, ref } from "vue";
export default {
  setup() {
    const state = reactive({
      count: ref(10),
    });
    const increaseCounter = () => {
      state.count += 1;
    };
    return { state, increaseCounter };
  },
};
</script>
