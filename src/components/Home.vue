<template>
  <div>
    <div>Hola {{ text }}</div>
    <p>Nombre: {{ firstName }}</p>
    <p>Apellido: {{ lastName }}</p>
    <p>Nombre completo: {{ fullName }}</p>
  </div>
</template>

<script>
import { ref, computed, toRefs } from "vue";
export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, context) {
    const { firstName, lastName } = toRefs(props);

    const text = ref("gerli");

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    console.log("context", context);

    return {
      text,
      fullName,
    };
  },
};
</script>
