<template>
    <ion-page>
      <ion-header :translucent="true">
        <ion-toolbar>
          <ion-title class="cart-title">¡Bienvenido!</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-card color="light" id="login-container">
        <div id="login-form" class="login-form">
          <strong>¡Bienvenido al carrito de compras!</strong>
          <p>Que bueno tenerte de regreso</p>
          <InputComponent v-model="user" id="user" name="user" label="Usuario: " placeholder="Introduce tu usuario" />
          <InputComponent v-model="password" type="password" id="password" name="password" label="Contraseña: " placeholder="Introduce tu contraseña" />
        </div>
        <div class="login-button">
          <ButtonComponent id="login" value="Iniciar Sesión" expand="full" @click="login" />
          <ButtonComponent id="forgotPassword" value="Olvidé mi contraseña" expand="full" />
          <ButtonComponent href="/pais" value="Ir al Pais" expand="full" />
          <ButtonComponent href="/departamento" value="Ir al Departamento" expand="full" />
          <ButtonComponent href="/ciudad" value="Ir a la Ciudad" expand="full" />
        </div>
      </ion-card>
    </ion-page>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  import { IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
  import ButtonComponent from '@/components/ButtonComponent.vue';
  import InputComponent from '@/components/InputComponent.vue';
  
  const user = ref('');
  const password = ref('');
  
  const login = () => {
    const username = user.value;
    const pass = password.value;
  
    if (username === 'abcd' && pass === 'abcd') {      
      window.location.href = "/dashboard";
    } else {
      console.log('Credenciales inválidas');
    }
  };
  </script>
  
  <style scoped src="../theme/login.css"></style>
  