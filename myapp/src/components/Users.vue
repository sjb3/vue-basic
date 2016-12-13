<template>
    <div class="users">
        <h1>Users</h1>
        <form v-on:submit="addUser">
            <input type="text" v-model="newUser.name" placeholder="Enter Name" />
            <br />
            <input type="text" v-model="newUser.email" placeholder="Enter Email" />
            <br />
            <input type="submit" value="Submit">
        </form>
        <ul>
             <li v-for="user in users">
                 {{user.name}}: {{user.email}}
            </li>
        </ul>
    </div>
</template>


<script>
    export default {
        name: 'users',
        data() {
            return {
                newUser: {},
                users: [
                    {
                        name: 'Jane Doe',
                        email: 'janedoe@mymail.com',
                        contacted: false
                    },
                    {
                        name: 'Jane Doe1',
                        email: 'janedoe1@mymail.com',
                        contacted: false
                    },
                    {
                        name: 'Jane Doe2',
                        email: 'janedoe2@mymail.com',
                        contacted: false
                    },
                ]
            }
        },
       methods: {
           addUser: function(e){
               console.log('add');
               e.preventDefault();    
           }
        },
  }
</script>

<style scoped>
    .users {
        color: #2d5e33;
        font-family: monospace;
    }
</style>