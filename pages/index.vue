<template>
  <div class="login-feild">
    <form class="login-form">
      <p class="login-text">e-mail</p>
        <input type="text" v-model="email" name="email" class="user-email" />
      <p class="login-text">password</p>
        <input type="text" v-model="password" name="password" class="user-password" />
      <div>
        <button type="submit" class="login-form-btn">ログイン</button>
      </div>
    </form>
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
}

.login-form {
  text-align: center;
  margin: auto;
  margin-top: 50%;
  width: 50vw;
}
.login-form-btn {
  width: 100%;
  height: 6vh;
  text-align: center;
}

.login-text {
  text-align: left;
  margin: 0%;
}

</style>
