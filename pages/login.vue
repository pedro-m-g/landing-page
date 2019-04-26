<template>
  <main class="content container login-page">
    <div class="login">
      <h1>Acceder</h1>
      <AppLogin />
    </div>
    <div class="signup">
      <h1>Regístrate</h1>
      <AppSignup />
    </div>
  </main>
</template>
<script>
import AppLogin from '@/components/AppLogin'
import AppSignup from '@/components/AppSignup'
export default {
  components: {
    AppLogin,
    AppSignup
  }
}
</script>
