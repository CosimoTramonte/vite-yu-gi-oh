
<script>
export default {
    name:"Card"
}
</script>

<template>
    <div class="ct-card">
        <div>
            <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
        </div>
        <h3>Titolo 1</h3>
        <h4>Titolo 2</h4>
    </div>
</template>

<style lang="scss" scoped>

.ct-card{
    width: calc(100% / 5);
    margin-bottom: 40px;
    text-align: center;

    div{
        width: 100%;
        height: 80%;
        img{
            width: 100%;
        }
    }
}

</style>