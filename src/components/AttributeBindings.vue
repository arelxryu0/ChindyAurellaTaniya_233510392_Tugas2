<template>
  <div>
    <h2>Attribute Bindings</h2>
    <img :src="imageSrc" alt="Logo" width="150" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageSrc: 'https://vuejs.org/images/logo.png'
    };
  }
}
</script>
