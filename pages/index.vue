<template>
  <div>
    <Nuxt/>
    <CountriesList/>
  </div>
</template>


<script lang="ts">
import Vue from 'vue'
import { countries } from '@/store'

export default Vue.extend({
  name: 'IndexPage',
  layout: 'americas',

  async asyncData() {
    await countries.index()
  },
})
</script>
<style lang="scss">
  body {
    @apply dark:bg-slate-800 dark:text-white
  }
</style>
