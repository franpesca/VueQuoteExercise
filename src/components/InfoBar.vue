<template>
    <div class="info-bar">
        <p> INFO: click on quote to delete it </p>
    </div>
</template>

<script>
    export default {
    
    }
</script>

<style scoped>
    .info-bar {
        text-align: center;
        font-size: 16px;
        margin: auto; 
        width: 65%;
        background-color: rgba(204, 204, 204, 0.426);
        border-radius: 10px;
        box-shadow: 3px 3px 3px 3px #ccc
    }
    .info-bar:hover{
        background-color: #f59696;
    }
</style>
