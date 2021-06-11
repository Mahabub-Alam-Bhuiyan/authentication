<template>

    <h3>Log In Your Account</h3>
    <form @submit.prevent="submit" class="log-in">
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input v-model="data.email" type="email " class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" required>
      </div>
      <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Password</label>
        <input v-model="data.password" type="password" class="form-control" id="exampleInputPassword1" required>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>

</template>


<script lang="ts">
import {reactive} from 'vue'
import {useRouter} from "vue-router";


export default {
  name: 'Login',
  setup(){
    const data = reactive({
      email: '',
      password: ''
    });

    const router = useRouter();

    const submit = async () =>{
      alert("Your Login Successful")
      await router.push('/')
    }

    return{
      data,
      submit
    }
  }
}
</script>

<style>

</style>
