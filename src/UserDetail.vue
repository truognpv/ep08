<template>
    <div class="component">
        <h3>Information User Details</h3>
        <p>List Details</p>
        <p>My name is: {{ name }} </p>
    </div>
</template>

<script>
export default{
    props: ['name']
    }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
