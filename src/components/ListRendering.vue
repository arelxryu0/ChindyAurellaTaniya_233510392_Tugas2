<template>
  <div>
    <h2>List Rendering</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Item 1', 'Item 2', 'Item 3']
    };
  }
}
</script>
