<script setup>
    const mensaje = () =>{
        console.log('Mensaje')
    }

    const borrarTarjeta = (index) => {
        console.log('Borrar tarjeta',index)
        emit('borrarTarjeta',index)
    }
    const emit = defineEmits(['borrarTarjeta'])

    const props = defineProps(

        { 
            name:{
                type: String,
                default: 'no name'
            },
            mail:{
                type: String,
                default:'no mail'
            },
            index:{
                type: Number
            }
        }
    )
</script>

<template>
    <div class="w-48 rounded shadow overflow-hidden m-5">
        <div class="inline-block align-top" @click="mensaje">
            <img src="https://picsum.photos/50" alt="">
        </div>
        <div class="inline-block pl-2">
            <h2 class="text-md font-semibold leading-0">{{props.name}}</h2>
            <p class="text-xs leading-0">{{props.mail}}</p>
        </div>
        <span class="inline-block ml-4 bg-red-700 text-white rounded py-0 px-2 m-2 hover:cursor-pointer hover:bg-red-900" @click="$event => borrarTarjeta(props.index)">
        X
        </span>
    </div>
    
</template>