<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome Developer! I'm {{name}} and {{age}}</p>
        <button @click="changeName">Change My Name</button>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail 
                v-bind:name="name"
                 @nameWasReset="name = $event"
                 v-bind:resetNameFn="resetName"
                 v-bind:userAge="age"></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-user-edit
                    v-bind:userAge="age"
                    v-on:ageWasEdit="age = $event">

                </app-user-edit>
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
                name: 'LieLove',
                age: 18
            }
        },
        methods: {
            changeName(){
                this.name = 'Pham Van Truong';
            },
            resetName(){
                this.name = 'LieLove'
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
