<template>
  <div class="login-feild">
    <div class="login-form">
      <p class="login-text">e-mail</p>
        <input type="text" v-model="email" name="email" class="user-email" />
      <p class="login-text">password</p>
        <input type="password" v-model="password" name="password" class="user-password" />
      <div>
        <button class="login-form-btn" @click="login">ログイン</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    login () {
      this.$router.push('/spot_list')
    }
  }
}
</script>

<style scoped >
.login-field {
  text-align: center;
  width: 50vw;
}

.user-email-field {
  margin: 0;
}
.user-email {
    height: 5vh;
    width: 100%;
    display: flex;
    text-align: center;
    box-sizing: border-box;
    color: black;
    text-align: left;
    margin-bottom: 16px;
    margin-top:2px;
    font-size: medium;
}
.user-password {
  width: 100%;
  height: 5vh;
  box-sizing: border-box;
  text-align: center;
  color: black;
  text-align: left;
  margin-bottom: 24px;
  margin-top: 2px;
  font-size: 16px;
}

.login-form {
  text-align: center;
  margin: auto;
  margin-top: 35vh;
  width: 80vw;
  font-size: larger;
}
.login-form-btn {
  width: 60%;
  height: 8vh;
  text-align: center;
  border: none;
  background-color:rgb(65, 176, 245);
  color: white;
  border-radius: 10px;
  font-size: larger;
}

.login-text {
  text-align: left;
  margin: 0%;

  font-size: larger;
}

</style>
