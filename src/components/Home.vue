<template>
  <div>Hola {{ text }} contador: {{ objeto }}</div>
</template>

<script>
import { ref, reactive, watch } from "vue";
export default {
  setup() {
    const text = ref("gerli");
    // setInterval(() => counter.value++, 500);
    const objeto = reactive({ contador: 0 });

    setInterval(() => objeto.contador++, 500);

    //watch
    watch(objeto, (valor, anterior) => {
      console.log("valor:", valor);
      console.log("anterior:", anterior);
    });

    return {
      text,
      objeto,
    };
  },
};
</script>
