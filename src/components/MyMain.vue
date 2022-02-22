<template>
    <main>
        <div class="contenitore-main">
            <div class="contenuto-main">
                Qui avremo il contenuto
            </div>
        </div>
    </main>
    
</template>

<script>
export default {
    name: 'MyMain',
}
</script>

<style scoped lang="scss">
    .contenitore-main{
        width: 100%; 
        background-color: #1c1c1c;   
    }
    .contenuto-main{
        width: 70%;
        margin: auto;
        height: 150px;
        display: flex;
        align-items: center;
        color: white;
    }
</style>