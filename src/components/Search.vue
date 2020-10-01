<template>
  <div class="row">
    <div class="col-12 q-pt-lg">
      <div class="row justify-center">
        <q-input outlined rounded
          class="input-content"
          input-class="input"
          bg-color="white">
          <template v-slot:prepend>
            <q-icon color="black" name="search" size="sm" />
          </template>
        </q-input>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  data () {
    return {}
  }
}
</script>
