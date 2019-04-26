<template>
  <form class="app-login">
    <div class="input">
      <label>Correo electrónico</label>
      <input type="email" name="" value="" />
    </div>
    <div class="input">
      <label>Contraseña</label>
      <AppPasswordField />
    </div>
    <button type="submit">
      Acceder
    </button>
  </form>
</template>
<script>
import AppPasswordField from '@/components/AppPasswordField'
export default {
  components: {
    AppPasswordField
  }
}
</script>
