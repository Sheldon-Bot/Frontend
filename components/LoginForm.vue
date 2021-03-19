<template>
  <div class="login">
    <div class="passcode-container">
      <h1 class="passcode">Enter Passcode</h1>
      <input ref="passcodeInput" type="password" id="code" name="passcodeInput">
      <button v-on:click="sendPassword()" type="button">Login</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginForm",

  methods: {

    async sendPassword() {
      const passCode = this.$refs['passcodeInput'].value
      if (!passCode) {
        return;
      }
      this.$http.setHeader('Content-Type', 'application/x-www-form-urlencoded')
      const data = await this.$http.$post('http://localhost:5001/auth', {auth: passCode})
        .catch(err => {
          console.log(err)
        })
      console.log(data)
      const authKey = data.code
      localStorage.setItem("authToken", authKey); //Saves auth key to local storage
      await this.$router.push('/control')
    }
  }

}
</script>

<style scoped>
.login {
  padding: 2em;
  display: flex;
  justify-content: center;
}

.passcode-container {
  width: 75vh;
  background-color: #243742;
  border-radius: 1em;
  display: flex;
  flex-direction: column;
  padding-bottom: 3em;

}

.passcode {
  letter-spacing: 2px;
  color: aliceblue;
  margin-left: auto;
  margin-right: auto;
  padding: 1em;
}

input {
  border-radius: 0.5em;
  border: darkgray;
  background-color: darkgray;
  display: block;
  margin-right: auto;
  margin-left: auto;
  height: 2em;
  width: 16em;
  outline: none;
  margin-bottom: 1em
}

button {
  width: 10em;
  border-radius: 0.5em;
  display: inline-block;
  margin-right: auto;
  margin-left: auto;
  background-color: #35495e;
  border: solid #35495e;
  outline: none;
  color: aliceblue;
}

button:hover {
  background-color: transparent;
  color: aliceblue;
}
</style>
