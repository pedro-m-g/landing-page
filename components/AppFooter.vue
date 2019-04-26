<template>
  <div class="app-footer">
    <div class="container">
      <small>&copy; D &amp; P {{ new Date().getFullYear() }}</small>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      contact: {
        email: '',
        message: ''
      }
    }
  }
}
</script>
