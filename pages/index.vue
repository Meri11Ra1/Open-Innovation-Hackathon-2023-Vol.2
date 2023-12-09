<template>
  <div>
    <form>
      <p><input type="text" v-model="email" placeholder="メールアドレス" name="email" /></p>
      <p><input type="text" v-model="password" placeholder="パスワード" name="password" /></p>
      <div>
        <button type="submit">ログイン</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      email: '',
      password: ''
    }
  }
}
</script>
