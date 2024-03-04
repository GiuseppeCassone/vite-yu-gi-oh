<script>
    export default {
        name: "AppNav",
    }
</script>

<template>
    <nav>
        <img src="/img/yu-gi-oh.png" alt="" id="logo">
        <h1>Yu-Gi-Oh Api</h1>
    </nav>
</template>

<style lang="scss">

    nav{
        display: flex;
        align-items: center;
        width: 100%;
        height: 100px;
        background-color: white;

        #logo{
            height: 100%;
            padding: 20px 40px;
        }

        h1{
            font-size: 44px;
            font-weight: 400;
        }
    }

</style>