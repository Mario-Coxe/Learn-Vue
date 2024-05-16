<template>
    <p>This p-tag belongs to 'CompOne.vue'</p>
</template>


<script>
export default {
    name: 'CompOne',
    data() {
        return {
            imgSrc: '../../public/qualidade.png'
        }
    }
}
</script>


<style scoped>
p {
    background-color: pink;
    width: 150px;
}
</style>