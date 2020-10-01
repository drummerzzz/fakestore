<template>
  <div
    class="bg-color header q-pt-sm">
    <q-btn @click="$store.commit('app/drawerMutation')" flat dense>
      <q-icon name="menu" size="lg"/>
    </q-btn>
    <div class="row q-pt-sm">{{title}} </div>
    <Search />
  </div>
</template>

<script>
import Search from 'components/Search'
export default {
  components: {
    Search
  },
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>
