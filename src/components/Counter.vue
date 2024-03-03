<template>
    <h2>Counter</h2>
    <p>{{ counter }} <sup>2</sup> = {{ squeareCounter }} </p>
</template>

<script>
export default {
    data(){
        return {
            counter: 5
        }
    },
    methods:{
        getSquareValue(){
            return this.counter * this.counter
        }
    },
    computed: {
        squeareCounter: function(){
            return this.counter * this.counter
        }
    }
}

</script>

<style>

</style>