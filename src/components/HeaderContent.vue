<template>
    <div>
        <select name="listadischi" id="listadischi">
            <option value="">all</option>
            <option v-for="(genreDisc, index) in filterGenre" :key="index" value="">{{genreDisc.genre}}</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'HeaderContent',
    data(){
        return{
            listGenre: []
        };
    },
    props:{
        Lista: Array
    },
    computed: {
        filterGenre(){
            /*for(let i = 0; i < this.Lista.length; i++){
                if(!this.listGenre.includes(this.Lista[i].genre)){
                    this.listGenre.push(this.Lista[i].genre)
                }
            }*/
            return this.Lista
        }
    },
}
</script>
<style lang scoped="scss">
    
</style>