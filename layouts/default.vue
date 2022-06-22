<template>
<div>
  <div class="main-header">
    <AppHeader />
    
  </div>
  <Nuxt />
    <div class="main-footer">
      <AppFooter />

    </div>
  </div>

</template>

<script>
  import AppHeader from "@/components/AppHeader"
  import AppFooter from "@/components/AppFooter"
  export default {
    components: {
      AppHeader,
      AppFooter
    }
  }

</script>
