<template>
    <div class="col-2 card-container m-3">
        <div class="d-flex justify-content-center">
            <img class="poster-card my-3" :src="SrcImage" :alt="Author">
        </div>
        <div class="d-flex flex-column justify-content-center align-items-center text-white">
            <h5 class="text-center ">{{Tytle}}</h5>
            <h6 class="text-secondary">{{Author}}</h6>
            <p class="text-secondary">{{Year}}</p>
        </div>
    </div>      
</template>

<script>
export default {
    name: 'DiscCard',
    props:{
        SrcImage: String,
        Tytle: String,
        Author: String,
        Year: String
    }

}
</script>

<style scoped lang="scss" >

.card-container{
    background-color:#2E3A46;
}
.poster-card{
    width: 150px;
    height: 150px;
}
</style>