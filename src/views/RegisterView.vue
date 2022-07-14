<template>
  <div class="row mt-3">
    <div class="col-md-4 offset-md-4">
      <div class="card">
        <div class="card-header bg-light">
          <h4>User Registeration</h4>
        </div>
        <form @submit.prevent="handleSubmit">
          <div class="card-body">
            <div class="mb-3">
              <label for="name">User Name</label>
              <input type="text" id="user" class="form-control" v-model="user.name">
            </div>
            <div class="mb-3">
              <label for="email">Email</label>
              <input type="email" id="email" class="form-control" v-model="user.email">
            </div>
            <div class="mb-3">
              <label for="password">Password</label>
              <input type="password" id="password" class="form-control" v-model="user.password">
            </div>
          </div>
        <div class="card-footer">
          <button type="submit" class="btn btn-primary">
              Register User
          </button>
        </div>
        </form>
      </div>
    </div>
  </div>

</template>





<script>
import { ref } from 'vue'

export default {
  setup() {
    
    const user = ref({ name:"", email:"", password:"" })

    async function handleSubmit() {
      
    }

    return {
      user,
      handleSubmit
    }
  },
}
</script>






<style>

</style>