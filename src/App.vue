<template>
  <div class="app">
    <div class="sidebar">
      <h2>Pertemuan 2 dan 3</h2>
      <ul>
        <li v-for="(item, index) in menu" :key="index" @click="currentComponent = item.component" :class="{ active: currentComponent === item.component }">
          {{ item.name }}
        </li>
      </ul>
    </div>
    <div class="content">
      <component :is="currentComponent" />
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import DeclarativeRendering from './components/DeclarativeRendering.vue'
import AttributeBindings from './components/AttributeBindings.vue'
import FormBindings from './components/FormBindings.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
import ComputedProperty from './components/ComputedProperty.vue'
import LifecycleRefs from './components/LifecycleRefs.vue'
import Watchers from './components/Watchers.vue'

export default {
  data() {
    return {
      currentComponent: 'Home',
      menu: [
        { name: 'Home', component: 'Home' },
        { name: 'Declarative Rendering', component: 'DeclarativeRendering' },
        { name: 'Attribute Bindings', component: 'AttributeBindings' },
        { name: 'Form Bindings', component: 'FormBindings' },
        { name: 'Conditional Rendering', component: 'ConditionalRendering' },
        { name: 'List Rendering', component: 'ListRendering' },
        { name: 'Computed Property', component: 'ComputedProperty' },
        { name: 'Lifecycle dan Template Refs', component: 'LifecycleRefs' },
        { name: 'Watchers', component: 'Watchers' }
      ]
    }
  },
  components: {
    Home,
    DeclarativeRendering,
    AttributeBindings,
    FormBindings,
    ConditionalRendering,
    ListRendering,
    ComputedProperty,
    LifecycleRefs,
    Watchers
  }
}
</script>

<style scoped>
.app {
  display: flex;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  height: 100vh;
  background: #f7f9fc;
}
.sidebar {
  width: 250px;
  background: #1f2937;
  color: white;
  padding: 20px;
  box-shadow: 2px 0 5px rgba(0,0,0,0.1);
}
.sidebar h2 {
  font-size: 20px;
  margin-bottom: 20px;
}
.sidebar ul {
  list-style: none;
  padding: 0;
}
.sidebar li {
  padding: 10px;
  margin-bottom: 5px;
  cursor: pointer;
  border-radius: 5px;
  transition: background 0.3s;
}
.sidebar li:hover, .sidebar li.active {
  background: #374151;
}
.content {
  flex: 1;
  padding: 40px;
  overflow-y: auto;
  background-color: white;
  border-left: 1px solid #ddd;
}
</style>
