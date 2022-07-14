<template>
<div class="row mt-3">
    <div class="col-md-4 offset-md-4">
      <div class="card">
        <div class="card-header bg-light">
          <h4>User Login</h4>
        </div>
        <form @submit.prevent="handleSubmit">
          <div class="card-body">
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
              Login User
          </button>
        </div>
        </form>
      </div>
    </div>
  </div>
</template>


<script>
import { ref } from '@vue/reactivity'

export default {
  setup() {
    
    const user = ref({email:"", password:""})

    async function handleSubmit() {
      alert(this.user.email + " " + this.user.password)
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