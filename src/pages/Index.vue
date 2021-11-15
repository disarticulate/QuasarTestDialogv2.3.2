<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageIndex',
  mounted () {
    this.$q.dialog({
      message: `This is Mounted at ${this.$options.name}`
    })
    this.$nextTick(() => {
      this.$q.dialog({
        message: `This is Mounted after $nextTick at ${this.$options.name}`
      })
    })
  }
})
</script>
