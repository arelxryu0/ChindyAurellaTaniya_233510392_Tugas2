<template>
  <div>
    <h2>Computed Property</h2>
    <input v-model.number="angka1" type="number" />
    +
    <input v-model.number="angka2" type="number" />
    =
    <strong>{{ hasil }}</strong>
  </div>
</template>

<script>
export default {
  data() {
    return {
      angka1: 0,
      angka2: 0
    };
  },
  computed: {
    hasil() {
      return this.angka1 + this.angka2;
    }
  }
}
</script>
