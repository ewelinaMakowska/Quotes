<template>
<div class="row">
    <app-quote v-for="(quote, index) in quotes" v-bind:key="index" @click.native="emitDeleteEvent(index)"> {{ quote }}</app-quote>
</div>
   
</template>

<script>

import Quote from './Quote.vue';

export default {
    props: ['quotes'],
    components: {
        appQuote: Quote
    },
    methods: {
        emitDeleteEvent(index) {
            this.$emit('quoteClicked', index);
            console.log('Quote clicked!')
        }
    }
}
</script>

<style>
</style>
