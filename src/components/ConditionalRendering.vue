<template>
  <div>
    <h2>Conditional Rendering</h2>
    <button @click="visible = !visible">Toggle</button>
    <p v-if="visible">Konten ini muncul jika visible = true</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: true
    };
  }
}
</script>
