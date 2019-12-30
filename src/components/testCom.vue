<template>
    <div>
        
        <h2>this for test differnt between computed and watch:</h2>
        <p>{{ fullName }}</p>
        
        <div>
            <label for="first">
                First Name
                <input id="first" type="text" v-model="firstName">
            </label>
            <label for="last">
                Last Name
                <input id="last" type="text" v-model="lastName">
            </label>
            
        </div>
    </div>
</template>

<script>
export default {
    name: 'testCom',
    data: function () {
        return {
            firstName: 'Nserallah',
            lastName: 'Ahmed',
            fullName: ''
        }
    },
    // computed: {
    //     fullName: function () {
    //         return this.firstName + ' dfgfggfh ' + this.lastName;
    //     }
    // },
    watch: {
       firstName: function (v) {
           this.fullName = v + ' ' + this.lastName
       },
        lastName: function (v) {
           this.fullName = this.firstName + ' ' + v
       }
       
    }
}
</script>

<style scoped>

</style>