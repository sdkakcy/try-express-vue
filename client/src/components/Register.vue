<template>
  <div class="register">
    <b-container>
      <h1>Register</h1>
      <b-row>
        <b-col>
          <b-form-input type="email" name="email" v-model="email" placeholder="E-posta">
          </b-form-input>
          <br>
          <b-form-input type="password" name="password" v-model="password" placeholder="Şifre">
          </b-form-input>
          <br>
          <b-button variant="primary" @click="register">Kayıt Ol</b-button>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService';

export default {
  name: 'Register',
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    async register() {
      const response = await AuthenticationService.register({
        email: this.email,
        password: this.password,
      });
      console.log(response.data);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
