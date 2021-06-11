<template>

    <h3>Sign up Your Account</h3>
    <form @submit.prevent="submit" class="log-in">
      <div class="mb-3">
        <label for="firstname" class="form-label">First Name :</label>
        <input v-model="data.firstname" type="text" class="form-control" id="firstname"  aria-describedby="emailName" required>
      </div>
      <div class="mb-3">
        <label for="lastname" class="form-label">Last Name :</label>
        <input v-model="data.lastname" type="text" class="form-control" id="lastname"  aria-describedby="emailName" required>
      </div>
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input v-model="data.email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" required>
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
  name: 'Register',
  setup(){
    const data = reactive({
      firstname: '',
      lastname: '',
      email: '',
      password: ''
    });

    const router = useRouter();

    const submit = async () =>{

      await router.push('/login')
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
