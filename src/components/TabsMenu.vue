<template>
  <q-card class="row justify-center bg-menu">
    <q-item clickable v-ripple
      v-for="item in menu" :key="item.icon"
      class="col-4 justify-center q-pa-lg">
      <q-icon
        :name="item.icon"
        color="primary"
        size="sm" />
    </q-item>
  </q-card>
</template>

<script>
export default {
  // name: 'ComponentName',
  data () {
    return {
      menu: [
        { icon: 'dashboard' },
        { icon: 'shopping_cart' },
        { icon: 'person' }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
.bg-menu
  background: rgba(248, 248, 248, 0.92)
  backdrop-filter: blur(27.1828px)

</style>
