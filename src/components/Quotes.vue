<template>
    <div class="quotes-wrapper">
        <app-quote v-for="(quote, index) in quotes" :key="index" @click.native="deleteQuote">
            {{quote}}
        </app-quote>
    </div>
</template>

<script>
    import Quote from './Quote.vue'
    export default {
    
        props: ["quotes"],
        components: {
            appQuote: Quote
        },
        methods: {
            deleteQuote(index){
                this.$emit('quoteDeleted',index)
            }
        }
    }
</script>

<style scoped>
    .quotes-wrapper {
        width: 800px;
        height: 250px;
        /* border: 1px solid teal; */
        margin: auto;
        margin-top: 3rem;
        margin-bottom: 2rem;
        border-radius: 10px;
        display:flex;
        flex-flow: wrap;
        align-content: center;
        justify-content: center;
        box-shadow:  3px 3px 3px 3px #ccc;
    }
    
</style>
