<template>
  <div class="login-container">
    <h1>Login Sewaku</h1>
    <form @submit.prevent="login">
      <div class="form-group">
        <label for="username">Username:</label>
        <input type="text" id="username" v-model="username" required>
      </div>
      <div class="form-group">
        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required>
      </div>
      <button type="submit">Login</button>
      <p>Belum punya akun? <a href="#">Daftar</a></p>

    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    login() {
      // Di sini Anda dapat menambahkan logika autentikasi Anda
      console.log("Username:", this.username);
      console.log("Password:", this.password);
      // Contoh: Validasi sederhana
      if (this.username === "user" && this.password === "user") {
        alert("Login berhasil!");

      } else {
        alert("Login gagal. Silakan coba lagi.");
      }
    }
  }
};
</script>

<style scoped>

.login-container {
  max-width: 600px;
  margin: 3rem auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
  text-align: center;
}

.form-group {
  margin-bottom: 10px;
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  display: block;
  width: 100%;
  padding: 10px;
  margin-bottom: 1rem;
  background-color: #1271d6;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-align: center;
}

button:hover {
  background-color: #3d6896;
}
</style>