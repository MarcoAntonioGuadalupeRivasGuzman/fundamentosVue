<template>
    <h2>Counter</h2>
    <p>{{ counter }} <sup>2</sup> = {{ squeareCounter }} </p>
    <div>
        <button @click="incrementCounter()" class="btn">+1</button>
        <button @click="decrementCounter()" class="btn">-1</button>
    </div>
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
        },
        incrementCounter(){
            return this.counter = this.counter +1;
        },
        decrementCounter(){
            return this.counter = this.counter -1;
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
.btn{
    background-color: #64BB87;
    border-radius: .5rem;
    border: 1px solid white;
    cursor: pointer;
    color: white;
    padding: 5px 15px;
    margin: 1rem;
    transition: 0.3s ease-in-out;
}

.btn:hover{
    background-color: #5aa67b;
    transition: 0.3s ease-in-out;
}
</style>