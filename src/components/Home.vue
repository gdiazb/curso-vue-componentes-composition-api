<template>
  <div>Hola {{ text }} contador: {{ objeto }}</div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  setup() {
    const text = ref("gerli");
    // setInterval(() => counter.value++, 500);
    const objeto = reactive({ contador: 0 });

    setInterval(() => objeto.contador++, 500);

    return {
      text,
      objeto,
    };
  },
};
</script>
