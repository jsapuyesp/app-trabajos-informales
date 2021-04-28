<template>
  <div class="register">
    <h1 class="title">Sign Up</h1>
    <form action class="form" @submit.prevent="register">
      <label class="form-label" for="#email">Email:</label>
      <input
        v-model="email"
        class="form-input"
        type="email"
        id="email"
        required
        placeholder="Email"
      />
      <label class="form-label" for="#password">Password:</label>
      <input
        v-model="password"
        class="form-input"
        type="password"
        id="password"
        placeholder="Password"
      />
      <label class="form-label" for="#password-repeat"
        >Repite la contraeña:</label
      >
      <input
        v-model="passwordRepeat"
        class="form-input"
        type="password"
        id="password-repeat"
        placeholder="Password"
      />
      <input class="form-submit" type="submit" value="Sign Up" />
    </form>
  </div>
</template>

<script>
import auth from "@/logic/auth";
export default {
  data: () => ({
    email: "",
    password: "",
    passwordRepeat: "",
    error: false
  }),
  methods: {
    async register() {
      try {
        await auth.register(this.email, this.password);
        this.$router.push("/")
      } catch (error) {
        console.log(error);
      }
    }
  }
};
</script>

<style scoped>

</style>
