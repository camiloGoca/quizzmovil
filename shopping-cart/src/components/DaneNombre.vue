<template>
  <ion-list>
 <ion-item>
      <ion-input label="Codigo Dane" placeholder="Digite su codigo dane"></ion-input>
    </ion-item>
    <ion-item>
      <ion-input label="Nombre" placeholder="Digite su nombre"></ion-input>
    </ion-item>
  </ion-list>
    </template>



    <script lang="ts">
  import { IonInput, IonItem, IonList } from '@ionic/vue';
  import { defineComponent } from 'vue';

  export default defineComponent({
    components: { IonInput, IonItem, IonList },
  });
</script>