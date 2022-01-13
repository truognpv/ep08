<template>
    <div class="component">
        <h3>Information User Details</h3>
        <p>List Details</p>
        <p>My name is: {{ name }} </p>
        <button @click="resetName">Reset name</button>
    </div>
</template>

<script>
export default{
    props: ['name'],
    methods: {
        resetName(){
            this.name= 'LieLove';
            this.$emit('nameWasReset', this.name);
        }
    }
    }
    
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
