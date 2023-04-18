<template>
    <div class="login-page">
      <div class="login-box">
        <h2 class="login-title">Welcome back!</h2>
        <form class="login-form">
          <div class="input-group">
            <label for="username">Username</label>
            <input type="text" id="username" v-model="username" required />
          </div>
          <div class="input-group">
            <label for="password">Password</label>
            <input type="password" id="password" v-model="password" required />
          </div>
          <button class="btn btn-primary login-btn" type="submit" @click.prevent="login">Log In</button>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: '',
      }
    },
    methods: {
      login() {
        // 登录逻辑
        // ...
        // 登录成功后跳转到用户列表页面
        this.$router.push('/user-list')
      },
    }
  }
  </script>
  
  <style>
  .login-page {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f5f5f5;
  }
  
  .login-box {
    width: 400px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: 40px;
  }
  
  .login-title {
    margin-top: 0;
    margin-bottom: 30px;
    font-size: 28px;
    font-weight: 600;
    color: #333;
  }
  
  .input-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
  }
  
  label {
    font-size: 16px;
    font-weight: 600;
    color: #333;
    margin-bottom: 8px;
  }
  
  input[type="text"],
  input[type="password"] {
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
    background-color: #f9f9f9;
  }
  
  .login-btn {
    padding: 10px;
    font-size: 16px;
    font-weight: 600;
    color: #fff;
    background-color: #007bff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
  }
  
  .login-btn:hover {
    background-color: #0069d9;
  }
  
  .login-btn:active {
    transform: translateY(2px);
  }
  
  @media (max-width: 768px) {
    .login-box {
      width: 90%;
      padding: 20px;
    }
  }
  </style>
  