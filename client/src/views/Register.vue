<template>
  <div class="register">
    <vue-headful
        :title="title"
        :description="description"
    />
    <img alt="Vue logo" src="../assets/logo.png">
    <RegisterForm/>
  </div>
</template>

<script>
// @ is an alias to /src
import RegisterForm from '@/components/Register.vue';

export default {
  name: 'Register',
  components: {
    RegisterForm,
  },
  data() {
    return {
      title: 'Kayıt Ol',
      description: 'Kayıt Ol',
    };
  },
};
</script>
