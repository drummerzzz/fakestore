<template>
  <q-drawer
    v-model="drawer"
    :width="$q.screen.lt.md ? 240 : 300"
    :breakpoint="700"
    overlay
    draggable
    content-class="bg-color text-primary">
    <q-scroll-area class="fit">
      <q-list separator>
        <q-img class="bg-primary" style="height: 150px">
          <div class="absolute-top bg-transparent">
            <div class="absolute-right">
              <q-btn @click="$store.commit('app/drawerMutation')"
                class="z-max" flat rounded dense>
                <q-icon name="close" size="lg"/>
              </q-btn>
            </div>
          </div>
          <div class="absolute-bottom bg-transparent">
            <q-avatar text-color="primary" class="bg-color q-mb-sm">JF</q-avatar>
            <!-- <q-avatar size="56px" class="q-mb-sm">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar> -->
            <div class="text-weight-bold">Name</div>
            <div>@username</div>
          </div>
        </q-img>
        <q-separator class="bg-color" size="16px" />
        <q-item v-for="item in menu" :key="item.label">
          <q-icon :name="item.icon" size="md" />
            <div class="q-ml-lg">{{item.label}}</div>
          </q-item>
      </q-list>
    </q-scroll-area>
  </q-drawer>
</template>

<script>
export default {
  computed: {
    drawer: {
      get () {
        return this.$store.state.app.drawer
      },
      set (v) {
        this.$store.commit('app/drawerMutation')
      }
    }
  },
  data () {
    return {
      menu: [
        { label: 'Inicio', icon: 'dashboard' },
        { label: 'Minhas Compras', icon: 'shopping_cart' },
        { label: 'Minha Conta', icon: 'person' }
      ]
    }
  }
}
</script>
