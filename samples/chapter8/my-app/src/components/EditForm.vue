<template>
  <div class="edit-form">
    <input ref="input" :value="message" @input="doUpdate" />
  </div>
</template>

<script>
export default {
  name: 'EditForm',
  computed: {
    message:{
      get() { return this.$store.getters.message },
      set(value) { this.$store.dispatch('doUpdate', value) }
    } 
  }
}
</script>
