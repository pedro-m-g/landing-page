<template>
  <div class="body">
    <div class="page">
      <AppNavbar />
      <nuxt />
    </div>
    <AppFooter />
  </div>
</template>
<script type="text/javascript">
import AppNavbar from '@/components/AppNavbar'
import AppFooter from '@/components/AppFooter'
export default {
  components: {
    AppNavbar,
    AppFooter
  }
}
</script>
