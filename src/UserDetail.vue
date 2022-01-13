<template>
    <div class="component">
        <h3>Information User Details</h3>
        <p>List Details</p>
        <p>My name is: {{ name }} </p>
        <p>My Age : {{userAge}} </p>
        <button @click="resetName">Reset name</button>
        <button @click="resetName">Reset Name</button>
    </div>
</template>

<script>
import {eventBus} from './main.js';
export default{
    props: {
        name: {
            type: Object
        },
        resetNameFn: Function,
        userAge: Number,

    },
    methods: {
        resetName(){
            this.name= 'LieLove';
            this.$emit('nameWasReset', this.name);
        }
    },
    created(){
        eventBus.$on('ageWasEdit', (age) => {
            this.userAge = age;
        })
    }
    }
    
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
