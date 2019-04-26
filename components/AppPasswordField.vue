<template lang="html">
  <div class="app-password-field">
    <input v-model="password" :type="type" name="" value="" />
    <div class="security-indicator" :class="securityClass">
      {{ securityStatus }}
    </div>
    <div class="visibility" @click="isVisible = !isVisible">
      <i :class="visibilityIcon"></i>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isVisible: false,
      password: ''
    }
  },
  computed: {
    security() {
      let p = 0
      if (this.password.length > 6) p += 2
      if (this.password.length > 10) p += 3
      if (/\d/.test(this.password)) p += 3
      if (/[A-Z]/.test(this.password)) p += 2
      return p
    },
    securityClass() {
      return {
        danger: this.security < 5,
        warning: this.security >= 5 && this.security < 8,
        success: this.security >= 8
      }
    },
    visibilityIcon() {
      return {
        fas: true,
        'fa-eye': !this.isVisible,
        'fa-eye-slash': this.isVisible
      }
    },
    securityStatus() {
      if (this.security < 5) return 'Insegura'
      if (this.security < 8) return 'Intermedia'
      return 'Segura'
    },
    type() {
      return this.isVisible ? 'text' : 'password'
    }
  }
}
</script>
