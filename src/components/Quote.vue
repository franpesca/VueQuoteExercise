<template>
    <div class="quote-wrapper">
        <slot></slot>
    </div>
</template>

<script>

</script>

<style scoped>
    * {
        box-sizing: border-box
    }
    
    .quote-wrapper {
        /* border: 1px solid rgb(0, 26, 83); */
        width: 25%;
        font-size: 18px;
        font-family: 'Times New Roman', Times, serif;
        background-color: #d8d7d7ab;
        border-radius: 13px;
        padding: 8px;
        margin: 8px;
        box-shadow: 2px 2px 2px 2px #ccc
    }
    
    .quote-wrapper {
        cursor: pointer;
    }
    
    .quote-wrapper:hover {
        background-color: #f59696;
    }
</style>
