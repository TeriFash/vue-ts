<template>
  <div class="main">
    <!-- <h1>{{ getData() }}</h1> -->

    <p v-text="getData()"></p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class MainComponent extends Vue {
  @Prop() private msg!: string;

  urlData = 'https://jsonplaceholder.typicode.com/posts'
  myData: { name: string } = { name: '' }

  getData () {
    fetch(this.urlData)
      .then(response => response.json())
      .then(data => console.log(data))
      .then(data => data)
  }
}
</script>

<style scoped lang="scss">

</style>
