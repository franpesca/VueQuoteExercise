<template>
    <div>
        <h4>Quotes Added</h4>
        <div class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" :style="{width: (quoteCount /maxQuotes) * 100 + '%'}">
                {{quoteCount}} / {{maxQuotes}}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>

<style>
    h4 {
        text-align: left;
        margin-left: 7rem;
    }
    
    .progress {
        width: 70%;
        height: 20px;
        border: 1px solid teal;
        /* margin: auto; */
        margin-bottom: 1rem;
        margin-left: 6rem;
        box-shadow: 1px 1px 1px 1px #ccc;
        border-radius: 10px;
    }
    
    .progress-bar {
        background-color: orange;
        width: 100%;
        margin-left: 0rem;
        height: 20px;
        
        border-radius: 10px;
    }
</style>
