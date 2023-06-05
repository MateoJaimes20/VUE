<script setup>
  import { ref } from 'vue';
  import CardComponent from './components/CardComponent.vue';
  const users = ref([
    {
      name:'Lionel Messi',
      mail:'papadecris@mail.com'
    },
    {
      name:'penaldo',
      mail:'hijodelgoat@mail.com'
    }
  ])
  const borrarTarjeta = (index) =>{
    console.log('Matar a', index)
    users.value.splice(index,1)
    console.log(users)
  }

  let name, mail

  const addUser = () => {
    const newUser = {
      name: name,
      mail: mail
    }

    users.value.unshift(newUser)

  }
</script>

<template>
  
  <h1 class="text-2xl">
    Hola mundo
  </h1>

  <input type="text" v-model="name" placeholder="Nombre" class="borde rounded">
  <br>
  <br>
  <input type="text" v-model="mail" placeholder="Mail" class="borde rounded">
  <br>
  <button class="bg-green-600 px-2 py-1 rounded mt-2" @click="addUser">Añadir</button>

  <div class="space-y-2">
    <CardComponent v-for="(user, index) in users" :key="index" :name="user.name" :mail="user.mail" :index="index" @borrarTarjeta="borrarTarjeta"/>
  </div>

</template>

<style scoped>

</style>
