<template>
  <hello-world>
    <template #body>The form is a test</template>
    <template #header><div style="background-color: red; color: white">Form title</div></template>
  </hello-world>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  components: {
    HelloWorld,
  },
}
</script>
