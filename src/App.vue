<template>
  <div>
    <the-basic-layout>
      <template v-slot>
        <router-view></router-view>
      </template>
    </the-basic-layout>
  </div>
</template>

<script>
import TheBasicLayout from "./layouts/TheBasicLayout.vue";
export default {
  name: 'App',
  components: {
    TheBasicLayout
  }
}
</script>

<style>
.app-font{
  font-family: 'AktivGrotesk', Arial, sans-serif;
  font-size: 40px;
}
</style>
