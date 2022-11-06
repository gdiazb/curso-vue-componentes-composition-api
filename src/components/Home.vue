<template>
  <div>Hola composition Api</div>
</template>

<script>
import { onMounted } from "vue";
export default {
  setup() {
    onMounted(() => {
      console.log("mounted");
    });
  },
};
</script>
