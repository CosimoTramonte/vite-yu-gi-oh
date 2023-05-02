
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
    <div class="ct-card">
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
    width: calc(100% / 5);
    margin-bottom: 40px;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    .divImage{
        width: 100%;
        margin-bottom: 10px;


        img{
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    .divName{
        width: 100%;

        h6{
            font-size: 18px;
        }
    }

    .divType{
        width: 100%;
    }

}

</style>