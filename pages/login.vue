<script lang="ts" setup>
const formData = reactive({
  email: '',
  password: '',
  isRemeberChecked: false,
})

const signInUser = () => {
  const router = useRouter();
  console.log(formData.email)
  console.log(formData.password)
  console.log(formData.isRemeberChecked)
  router.push('/')
}
</script>

<template>
  <div class="h-screen">
    <div class="flex flex-row items-center justify-center h-full">
      <div class="flex flex-col mb-48">
        <p class="text-5xl text-white font-bold text-center mb-6">Admin Panel</p>
        <div class="card card-bordered w-96 bg-base-100 shadow-xl">
          <div class="card-body">
            <h2 class="card-title justify-center text-white text-4xl mb-4">Sign In</h2>
            <form @submit.prevent="signInUser">
              <input v-model="formData.email" type="email" placeholder="Email" class="input input-bordered w-full max-w-xs mb-4" />
              <input v-model="formData.password" type="password" placeholder="Password" class="input input-bordered w-full max-w-xs" />
              <div class="card-actions justify-between mt-6">
                <div class="form-control">
                  <label class="label cursor-pointer">
                    <input type="checkbox" :checked="formData.isRemeberChecked" class="checkbox checkbox-primary mr-2" />
                    <span class="label-text">Remember me</span>
                  </label>
                </div>
                <button class="btn btn-primary">Login</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
