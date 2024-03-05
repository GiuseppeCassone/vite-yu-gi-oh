<script>

    export default {
        name: 'AppLoader',
    }
</script>

<template>
    <div class="loader">
        LOADING
        <div class="loader-bar"></div>
    </div>
</template>

<style lang="scss">

    .loader{
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        font-size: 40px;
        font-weight: bold;
        background-color: #D48F38;
    }

    /* HTML: <div class="loader"></div> */
    .loader-bar {
        width: 200px;
        height: 20px;
        margin-left: 30px;
        background: 
            linear-gradient(90deg, #0000 ,orange) left -50px top 0/50px 20px no-repeat 
            lightblue;
        animation: l2 1s infinite linear;
    }
     @keyframes l2 {
        100% {background-position: right -50px top 0}
    }

</style>