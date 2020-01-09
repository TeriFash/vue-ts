<template>
  <div class="dashboard">
    <h1>This is an dashboard page</h1>

    <MainComponent/>
  </div>
</template>

<script>
// @ is an alias to /src
import MainComponent from '@/components/MainComponent.vue'

export default {
  name: 'dashboard',
  components: {
    MainComponent
  }
}
</script>
