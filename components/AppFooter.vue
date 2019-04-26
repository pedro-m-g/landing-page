<template>
  <div class="app-footer">
    <form class="container">
      <h1>Contáctanos</h1>
      <div class="input">
        <label>Correo electrónico</label>
        <input
          v-model="contact.email"
          type="email"
          placeholder="Correo electrónico"
        />
      </div>
      <div class="input">
        <label>Mensaje</label>
        <textarea v-model="contact.message" placeholder="Mensaje..."></textarea>
      </div>
      <button type="submit">
        Enviar mensaje
      </button>
    </form>
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
