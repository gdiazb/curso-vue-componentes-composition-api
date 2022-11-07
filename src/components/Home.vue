<template>
  <div>
    <div>Hola {{ text }}</div>
    <p>Nombre: {{ firstName }}</p>
    <p>Apellido: {{ lastName }}</p>
    <p>Nombre completo: {{ fullName }}</p>
  </div>
</template>

<script>
import { ref, computed } from "vue";
export default {
  setup() {
    const text = ref("gerli");
    const firstName = ref("Geraldine");
    const lastName = ref("Díaz Barrr");

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    return {
      text,
      firstName,
      lastName,
      fullName,
    };
  },
};
</script>
