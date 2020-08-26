<template>
  <div>
    <v-btn @click="$auth.loginWith('auth0')">Sign In</v-btn>
    <div>
      you are loginned as {{this.$auth.$state}}
    </div>
    <div>
      <v-btn>{{ this.res }}</v-btn>
    </div>
  </div>
</template>
<script>
  import axios from 'axios'

  export default {
    data: {
      res: ''
    },
    components: {
    },
    mounted() {
      this.res = axios.get("localhost:8080", {"headers": {
          "authorization": localStorage.getItem("auth0_token.auth0")
        }
      })
    }
}
</script>
