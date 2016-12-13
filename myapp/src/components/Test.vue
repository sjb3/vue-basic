<template>
    <div class="test">
         
        <h1>{{title}}</h1>
        <p v-if="showName">my name is : {{user.firstName}}</p>
        <ul>
            <li v-for="item in items">{{item.title}}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'test',
        data() {
            return {
                title: 'hello Human!',
                user: {
                    firstName: 'Justin',
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
        }
   }
</script>

<style scoped>
</style>