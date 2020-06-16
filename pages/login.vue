<template>
  <div class="">
      <div class="p-12 shadow rounded max-w-lg bg-white">
        <h1 class="text-4xl text-center">Login to Hourglass</h1>
        <form @submit.prevent="login">
          <div class="p-2">
            <label class="block pb-1">Email</label>
            <input v-model="email" type="email" name="email" required autofocus placeholder="Enter email address" class="border-2 p-1 w-full" />
          </div>
          <div class="p-2">
            <label class="block pb-1">Password</label>
            <input v-model="password" type="password" name="password" required autofocus class="border-2 p-1 w-full" />
          </div>
          <div class="p-2">
            <button type="submit" class="px-5 py-2 bg-secondary text-white">Login</button>
          </div>
        </form>

      </div>
  </div>
</template>

<script>
  import swal from 'sweetalert2';

  export default {
    data() {
      return {
        email: '',
        password: '',
      }
    },
    layout: 'unauth',
    methods: {
      login(){
        this.$axios.post('/login', {
          email: this.email,
          password: this.password
        }).then(function (response) {
          console.log(response.data);
          localStorage.setItem('token', response.data.csrf_token);
        }).catch(function (error) {
          console.log(error);
          localStorage.removeItem('token');
        });
      }
    }
  }
</script>
