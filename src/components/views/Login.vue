<template>
    <div class="login-container">
      <div class="login-box">
        <h2>Inicio de sesión</h2>
        <form @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="email">Correo</label>
            <input type="email" id="email" v-model="email" placeholder="persona@correo.com" required />
          </div>
          <div class="form-group">
            <label for="password">Contraseña</label>
            <input type="password" id="password" v-model="password" placeholder="*************" required />
          </div>
          <div class="form-group checkbox">
            <input type="checkbox" id="rememberMe" v-model="rememberMe" />
            <label for="rememberMe">Recordar contraseña</label>
          </div>
          <div class="form-group">
            <button type="submit" class="btn">Continuar</button>
          </div>
          <div class="register-link">
            ¿Necesitas una cuenta? <a href="/register">¡Regístrate!</a>
          </div>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: '',
        rememberMe: false
      };
    },
    methods: {
      handleSubmit() {
        console.log('Email:', this.email);
        console.log('Password:', this.password);
        console.log('Remember Me:', this.rememberMe);
      }
    }
  };
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 70vh;
    background-color: #e0e0e0;
  }
  
  .login-box {
    background-color: #6b6bca;
    padding: 40px;
    border-radius: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 400px;
  }
  
  h2 {
    color: white;
    text-align: center;
  }
  
  .form-group {
    margin-bottom: 15px;
  }
  
  label {
    display: block;
    color: white;
    margin-bottom: 5px;
  }
  
  input[type="email"],
  input[type="password"] {
    width: 100%;
    padding: 8px;
    border: none;
    border-radius: 4px;
  }
  
  .checkbox {
    display: flex;
    align-items: center;
  }
  
  .checkbox input {
    margin-right: 5px;
  }
  
  .btn {
    width: 100%;
    padding: 10px;
    background-color: #4848a2;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .btn:hover {
    background-color: #3a3a82;
  }
  
  .register-link {
    text-align: center;
    margin-top: 10px;
  }
  
  .register-link a {
    color: white;
    text-decoration: none;
  }
  
  .register-link a:hover {
    text-decoration: underline;
  }
  </style>
  