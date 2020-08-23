<template>
  <div>
    <v-btn @click="$auth.loginWith('auth0')">Sign In</v-btn>
    <div>
      you are loginned as {{this.$auth.$state}}
    </div>
  </div>
</template>
<script>

export default {
  components: {
  }
}
</script>
