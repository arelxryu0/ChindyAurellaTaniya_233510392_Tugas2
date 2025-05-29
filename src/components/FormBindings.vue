<template>
  <div>
    <h2>Form Bindings</h2>
    <input v-model="name" placeholder="Masukkan nama" />
    <p>Halo, {{ name }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ''
    };
  }
}
</script>
