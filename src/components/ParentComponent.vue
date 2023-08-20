<script setup>
    import { reactive,ref } from 'vue'
    import ChildComponent from './ChildComponent.vue';

    const persons = reactive({
            'name'  : 'Shahinul Islam',
            'age'   : 29,
            'occupasion' : 'Frontend Designer',
            'projects' : [
                {'name' : 'POS', 'link' : 'https://shahinulislam.com'},
                {'name' : 'LMS management', 'link' : 'https://shahinulislam.com'}
            ],

            'message'   : 'I am Frontend Designer'
        });
</script>

<template>
    <div class="mt-10">
        <h1 class="text-black-900 text-xl my-5">Parent Component:</h1>
        <h2 class="text-black text-l ">Name : {{ persons.name }}</h2>
        <h2 class="text-black text-l ">Age : {{ persons.age }}</h2>
        <h2 class="text-black text-l ">Occupasion : {{ persons.occupasion }}</h2>
        <h2 class="text-black text-l ">Message : {{ persons.message }}</h2>
        <h2 class="text-black text-l mt-5 mb-3">Projects:</h2>
        <ul class="list-disc">
            <li class="ml-5" v-for="(project, index) in persons.projects" :key="index">{{ project.name }}</li>
        </ul>
    </div>

    <ChildComponent v-model:message="persons.message" ></ChildComponent>
</template>

<style scoped>

</style>