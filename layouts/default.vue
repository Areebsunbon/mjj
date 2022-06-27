<template>
<div>
  <header class="main-header">
    <AppHeader />
    
  </header>
  <Nuxt />
    <footer class="main-footer">
      <AppFooter />

    </footer>
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
