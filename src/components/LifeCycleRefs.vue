<template>
  <div>
    <h2>Lifecycle dan Template Refs</h2>
    <input ref="inputBox" />
  </div>
</template>

<script>
export default {
  mounted() {
    this.$refs.inputBox.focus();
  }
}
</script>
