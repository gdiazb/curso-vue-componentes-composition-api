<template>
  <div>
    <button @click="toggle">click aquí</button>
    <teleport to="body">
      <div v-show="showModal" class="container-modal">
        <div class="modal">
          <h3 class="modal__title">Titulo</h3>
          <p class="modal__txt">
            Lorem ipsum dolor sit amet consectetur adipisicing elit
          </p>
          <button @click="toggle" class="modal__btn">Cerrar</button>
        </div>
      </div>
    </teleport>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    toggle() {
      this.showModal = !this.showModal;
    },
  },
};
</script>
