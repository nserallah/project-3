<template>
    <div>
        <hr>
        <h2>this is test for (Emit) from child to parent:</h2>
        <p>{{ count }}</p>
        <button @click="addOne()">Increment</button>
    </div>
</template>

<script>
export default {
    name: 'emitTest',
    props: ['count'],
    data: function () {
        return {
            
        }
    },
    methods: {
        addOne: function () {
            //return this.count++;
            this.$emit('addOne');
        }
    }
}
</script>

<style scoped>

</style>