<template>
  <b-col class="mt-2" md="4" sm="6" align="center">
    <b-card
      :title="name"
      img-src="https://desktopmania.ru/pics/00/86/71/DesktopMania.ru-86710-300x187.jpg"
      img-alt="Job-info"
      img-top
      tag="article"
      style="max-width: 20rem"
      class="mb-2"
      footer="Card Footer"
    >
      <b-card-text>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt,
        excepturi.
      </b-card-text>
      <b-button
        v-b-tooltip.hover
        title="Tooltip content"
        v-b-modal="modalId"
        variant="primary"
        >Go somewhere</b-button
      >
      <b-modal :id="modalId" title="BootstrapVue">
        <p class="my-4">Hello from modal!</p>
      </b-modal>
    </b-card>
  </b-col>
</template>

<script>
export default {
  props: ["name", "id"],
  computed: {
    modalId() {
      return `modal-${this.id}`;
    },
  },
};
</script>

<style scoped></style>
