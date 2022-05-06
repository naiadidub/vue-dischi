<template>
    <div class="col-2">
        <div class="card" style="width: 18rem;">
            <img :src="SrcImage" class="card-img-top" :alt="Author">
        <div class="card-body">
        <h5 class="card-title">{{Tytle}}</h5>
        <h6>{{Author}}</h6>
        <p>{{Year}}</p>
  </div>
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

<style lang="scss" scoped>

</style>