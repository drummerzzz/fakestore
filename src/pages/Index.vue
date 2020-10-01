<template>
  <q-page class="bg-color">
    <div class="row justify-center q-py-lg" >
      <Card v-for="item in items" :key="item.id" :card="item" />
    </div>
  </q-page>
</template>

<script>
import Card from 'components/Card'
import axios from 'axios'

export default {
  name: 'PageIndex',
  components: {
    Card
  },
  data () {
    return {
      items: []
    }
  },
  methods: {
    loadData () {
      const url = 'https://jsonplaceholder.typicode.com/photos'
      axios.get(url).then(resp => {
        this.items = resp.data.splice(0, 50)
      })
    }
  },
  created () {
    this.loadData()
  }
}
</script>
