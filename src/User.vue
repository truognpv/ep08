<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome Developer! I'm Sky Albert</p>
        <button @click="changeName">Change My Name</button>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail v-bind:name="name" @nameWasReset="name = $event"></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-user-edit></app-user-edit>
            </div>
        </div>
    </div>
</template>

<script>
    import UserDetail from './UserDetail.vue';
    import UserEdit from './UserEdit.vue';

    export default {
        
        data: function(){
            return {
                name: 'LieLove'
            }
        },
        methods: {
            changeName(){
                this.name = 'Pham Van Truong';
            }
        },
        components: {
            appUserDetail: UserDetail,
            appUserEdit: UserEdit
        }
    }
</script>

<style>
    .component {
        background-color: lightblue;
    }
</style>
