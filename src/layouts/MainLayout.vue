<template>
  <q-layout view="lHh Lpr lFf" class="bg-color">
    <div class="q-px-lg">
      <Drawer />
      <Header title="Titulo da página" />
    </div>
    <br><br>
    <q-scroll-area class="q-pb-lg"
      style="height: 70vh; min-width: 92vw;">
      <q-page-container class="q-px-lg">
        <router-view />
      </q-page-container>
    </q-scroll-area>
    <TabsMenu class="fixed-bottom" />
  </q-layout>
</template>

<script>
import TabsMenu from 'components/TabsMenu'
import Header from 'components/Header'
import Drawer from 'components/Drawer'
export default {
  name: 'MainLayout',
  components: {
    TabsMenu,
    Header,
    Drawer
  }
}
</script>
