<template>
  <div class="home">
    <main-container>
      <bitcoin-get />
    </main-container>
  </div>
</template>


<script>
  // @ is an alias to /src
  //import HelloWorld from '@/components/HelloWorld.vue'
  import mainContainer from '../components/MainContainer.vue'
  import BitcoinGet from '../components/BitcoinGet.vue'
  


  export default {
    name: 'Home',
    components: {
      mainContainer,
      BitcoinGet,
    }
  }
</script>
