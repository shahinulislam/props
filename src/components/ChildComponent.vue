<script setup>
   const props  = defineProps(['message']);
   const emit   = defineEmits(['update:modelValue']);

   function messageEmitted (){
     props.name = emit('update:message','Hi, I am Shahinul Islam!')
   }

</script>

<template>
    <div class="mt-10">
        <h1 class="text-black-900 text-xl my-5">Chiled Component:</h1>
        <h2 class="text-black text-xl my-5">Message : <span class="text-green-500 hover:text-purple-700">{{ message }}</span></h2>

        <button @click="messageEmitted ()" class="bg-blue-500 hover:bg-blue-600 text-white font-bold my-8 py-2 px-4 rounded">
            Button
        </button>
    </div>
</template>

<style scoped>

</style>