<template>
  <div class="mycard-content bg-color col-6 col-sm-4 col-md-3 col-lg-2">
    <div class="mycard" :style="{backgroundImage: `url(${card.thumbnailUrl})`}"></div>
    <div
      class="relative-position col bg-white text-primary text-h6 text-weight-bold q-pa-sm"
      style="height: 50px">
      Item {{card.id}}
      <div class="absolute-right q-pa-sm">
        <q-icon name="add_shopping_cart" size="sm"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  props: {
    card: {
      type: Object,
      required: true
    }
  },
  data () {
    return {}
  }
}
</script>

<style lang="sass">
.mycard-content
  margin-bottom: 0.2em
  padding: 0.3em

.mycard
  width: 100%
  height: 150px
  background-color: #DBD8DD
  background-size: 100% 100%
  border-radius: 8px 8px 0px 0px
</style>
