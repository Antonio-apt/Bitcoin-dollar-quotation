<template>
  <div class="quotation">
    <main-container>
      <dolar-get />
    </main-container>
  </div>
</template>


<script>
  // @ is an alias to /src
  //import HelloWorld from '@/components/HelloWorld.vue'
  import mainContainer from '@/components/MainContainer.vue'
  import DolarGet from '@/components/DolarGet.vue'

  export default {
    name: 'Quotation',
    components: {
      mainContainer,
      DolarGet
    }
  }
</script>

