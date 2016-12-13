<template>
    <div class="test">
         
        <h1>hello {{title}}!</h1>
        <input type="text" v-model="title"><br />
        <button v-on:click="IP">IP addy</button>
        <p v-if="showName">my name is : {{user.firstName}} {{user.lastName}}</p>
        <ul>
            <li v-for="item in items">{{item.title}}</li>
        </ul>
        <label> First Name: </label><input type="text" v-model="user.firstName"><br />
        <label> Last Name: </label><input type="text" v-model="user.lastName">

        <h3>{{fullName}}</h3>
        <h2>{{msg}}</h2><hr />
    </div>
</template>

<script>
    export default {
        name: 'test',
        props: {
            msg: {
                type: String,
                default: 'Foobar'
            }
        },
        data() {
            return {
                title: 'Human',
                user: {
                    firstName: 'John',
                    lastName: 'Doe'
                },
                showName: true,
                items: [
                    {title: 'Item One'},
                    {title: 'Item Two'},
                    {title: 'Item Three'},
                    {title: 'Item Four'}
                ]
            }
        },
        methods: {
            IP: function(){
                alert('173.250.160.234 ');
            }
        },
        computed: {
            fullName: function(){
                return this.user.lastName+', ' + this.user.firstName
            }
        }
       
   }
</script>

<style scoped>
    
</style>