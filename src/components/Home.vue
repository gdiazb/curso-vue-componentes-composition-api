<template>
  <div>
    <div>Hola {{ text }}</div>
    <p>Nombre: {{ firstName }}</p>
    <p>Apellido: {{ lastName }}</p>
    <p>Nombre completo: {{ fullName }}</p>
    <p>Username: {{ username }}</p>
    <button ref="btnHome">Click</button>
  </div>
</template>

<script setup>
import { defineProps, ref, computed, toRefs, inject, watch } from "vue";

const props = defineProps({
  firstName: String,
  lastName: String,
});

const { firstName, lastName } = toRefs(props);

const text = ref("gerli");

const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});

const username = ref(inject("userName"));

// console.log("context", context);

const btnHome = ref(null);

watch(btnHome, (valor) => {
  console.log(valor);
});
</script>
