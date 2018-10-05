<template>
    <div>
        <button class="btn btn-primary" @click="increment">Increment</button>
        <button class="btn btn-primary" @click="decrement(100)">Decrement</button>
        <hr>
        <button class="btn btn-primary" @click="AsyncIncrement({by: 50, duration: 500})">Async Increment</button>
        <br><br>
        <button class="btn btn-primary" @click="asyncDecrement({by: 50, duration: 500})">Async Decrement</button>
    </div>
</template>

<script>
    import {mapActions} from 'vuex';

    export default {
        methods: {
            ...mapActions([
                'increment',
                'decrement',
                'asyncIncrement',
                'asyncDecrement'
            ]),
        }
    }
</script>