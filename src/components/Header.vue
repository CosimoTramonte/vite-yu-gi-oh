
<script>
export default {
    name: "Header"
}
</script>

<template>

    <div>
        <img src="../../public/logo.png" alt="logo">
        <h1>Vite Yu Gi Oh</h1>
    </div>

</template>

<style lang="scss" scoped>

    @use "../scss/partials/utilities";

    div{
        display: flex;
        align-items: center;
        padding: 20px;

        img{
            width: 50px;
        }

        h1{
            font-size: 40px;
            margin-left: 20px;
        }
    }

</style>