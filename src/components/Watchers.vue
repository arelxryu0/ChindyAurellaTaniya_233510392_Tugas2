<template>
  <div>
    <h2>Watchers</h2>
    <input v-model="nama" placeholder="Masukkan nama" />
    <p>{{ pesan }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nama: '',
      pesan: ''
    };
  },
  watch: {
    nama(newValue) {
      this.pesan = `Nama diubah menjadi: ${newValue}`;
    }
  }
}
</script>
