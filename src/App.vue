<template>
  <main>
      <div>
        <Navbar/>
      </div>
      <div>
        <RouterView/>
      </div>
  </main>
</template>

<script>
import { RouterView } from 'vue-router';
import Navbar from './components/Navbar.vue'
import Message from './components/icons/Message.vue';
export default {
components:{
  RouterView,
  Navbar,
  Message
}
}
</script>

<style>

</style>