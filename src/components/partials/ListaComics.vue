<template>
    <div class="banner">
        <img :src="img" alt="">
        <h3>{{titolo}}</h3>
    </div>
</template>

<script>
export default {
    name: 'ListaComics',
    props: {
        'img': String,
        'titolo': String,
    },
}
</script>

<style scoped lang="scss">
    .banner{
        width: 15%;
        margin: 50px 10px;

        img{
            width: 100%;
            height: 170px;
            object-fit: cover;
            object-fit: cover;
            object-position: top;
        }
    }
</style>