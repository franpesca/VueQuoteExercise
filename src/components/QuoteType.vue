<template>
    <div>
        <form @keydown.enter="createQuote">
            <div class="form-container">
                <label style='display:block;'> Quote of the day.. </label>
                <textarea class="textarea" placeholder="Type in here your quote..." v-model="quote"></textarea>
            </div>
            <div>
                <button @click.prevent="createQuote" class="button"> ADD QUOTE </button>
            </div>
        </form>
        <!-- <div class="quote-wrapper">     -->
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            }
        },
        methods: {
            createQuote() {
                if (this.quote.length < 1) {
                    alert('Please, type your quote before submitting it')
                } else {
                    this.$emit('quoteAdded', this.quote);
                    this.quote = '';
                }
            }
        }
    }
</script>

<style scoped>
    label {
        font-weight: 500;
        font-size: 23px;
    }
    
    .textarea {
        padding: 20px;
        box-shadow: 1px 1px 1px 1px #ccc;
        border-radius: 10px;
        font-size: 17px;
        font-style: oblique;
        text-align: center;
    }
    
    .button {
        padding: 10px;
        box-shadow: 1px 1px 1px 1px #ccc;
        border-radius: 4px;
        background-color: orange;
        color: white;
        font-weight: 600;
    }
    
    .button:hover {
        color: orange;
        background-color: white;
    }
    
    .quote-wrapper {
        width: 400px;
        height: 250px;
        border: 3px solid teal;
        margin: auto;
        margin-bottom: 1rem;
        background-color: #fff;
        border-radius: 5px;
        padding: 20px;
        font-size: 14px;
    }
    
    .quote {
        cursor: pointer;
    }
    
    .quote:hover {
        background-color: #ccc;
    }
</style>

