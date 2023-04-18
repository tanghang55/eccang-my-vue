<template>
    <div class="register-page">
      <h2 class="register-title">Create an Account</h2>
      <form class="register-form" @submit.prevent="registerUser">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <button type="submit" class="register-btn">Create Account</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        password: '',
      }
    },
    methods: {
      registerUser() {
        // TODO: handle user registration
        console.log('User registered:', this.name, this.email, this.password)
        // reset form fields
        this.name = ''
        this.email = ''
        this.password = ''
      },
    },
  }
  </script>
  
  <style>
  .register-page {
    padding: 40px;
  }
  
  .register-title {
    font-size: 28px;
    font-weight: 600;
    margin-top: 0;
    margin-bottom: 30px;
  }
  
  .register-form {
    width: 400px;
    max-width: 100%;
  }
  
  .form-group {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    font-weight: 600;
    margin-bottom: 5px;
  }
  
  input {
    display: block;
    width: 100%;
    padding: 10px;
    font-size: 16px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .register-btn {
    display: block;
    width: 100%;
    padding: 10px;
    font-size: 16px;
    color: #fff;
    background-color: #4CAF50;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>
  