
<script>
export default {
    name:"Card",
    props:{
        name: String,
        type: String,
        img: Object,
    }
}
</script>

<template>
    <div class="ct-card p-0">
        <div class="divImage">
            <img :src="img.image_url" :alt="name">
        </div>
        <div class="divName">
            <h6 class="fw-bold m-0">{{name}}</h6>
        </div>
        <div class="divType">
            <p class="m-0">{{type}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>

.ct-card{
    width: calc(100% / 5 - 20px);
    margin: 0 10px 40px;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #D48F38;
    border-radius: 0px 0px 10px 10px;
    box-shadow: 0px 0px 5px black;

    .divImage{
        width: 100%;
        margin-bottom: 10px;
        transition: all 0.3s;

        &:hover{
            transform: scale(1.05);
        }

        img{
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    .divName{
        width: 100%;
        padding: 0 2px;

        h6{
            font-size: 18px;
            color: white;
        }
    }

    .divType{
        width: 100%;
    }

}

</style>