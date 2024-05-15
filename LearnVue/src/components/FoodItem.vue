<template>
    <div>
        <h2>{{ foodName }}</h2>
        <img src="../../public/qualidade.png" v-show="foodIsFavorite">
        <p>{{ foodDesc }}</p>
        <button v-on:click="toggleFavorite">Favorite</button>
    </div>
</template>

<script>

export default {
    //props: ['foodName', 'foodDesc', 'isFavorite'],
    props: {
        foodName: { type: String, default: 'Food Name' },
        foodDesc: {
            type: String, reuired: false, default: 'This is the default description',
            validator: function (value) {
                if (20 < value.length && value.length < 50) {
                    return true;
                }
                else {
                    return false;
                }
            }
        },
        isFavorite: {
            type: Boolean,
            required: false,
            default: false
        }
    },
    data() {
        return {
            foodIsFavorite: this.isFavorite
        }
    },
    methods: {
        toggleFavorite() {
            this.foodIsFavorite = !this.foodIsFavorite;
        }
    },

};

</script>

<style>
img {
    height: 1.5em;
    float: right;
}
</style>