<template>
    <div id="main-container">
        <slot class="slot"></slot>
    </div>
</template>

<script>
    export default {
        name: 'mainContainer'
    }
</script>


<style  lang="scss" >
    #main-container {
        align-items: center;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        text-align: center;

        h1 {
            color: rgb(170, 182, 197);
        }
    }


    #teste {

        //margin: 0 auto;
        position: relative;
        margin-top: 5%;
        padding-top: 50px;
        width: 30%;
        box-shadow: 2px 2px 10px rgb(43, 42, 42);
        line-height: 1.7;
        height: 300px;
        background-color: #141a16;
        color: #52685f;
        border-radius: 15px;
        word-wrap:  break-word;

    }

    .lighten {
        color: rgb(170, 182, 197);
    }
</style>