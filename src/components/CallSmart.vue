<template>
<div class="row">
    <div v-for="recipe in recipes" v-bind:key="recipe">
        <Recipes    v-bind:img="recipe.thumbnail"
                    v-bind:title="recipe.title"
                    v-bind:ingredients="recipe.ingredients"
                    v-bind:link="recipe.href"
        ></Recipes>
    </div>
</div>
</template>

<script>
import Recipes from './IndexDumb.vue'
export default {
    name: 'CallSmart',
    components: {
        Recipes
    },
    data() {
        return {
            recipes: []
        }
    },
    beforeMount: function(){
    const app = this;
    const conversionURL = 'https://cors-anywhere.herokuapp.com/'
    const url = 'http://www.recipepuppy.com/api/'

    fetch(conversionURL + url)
    .then(function(response) {
            return response.json();
        })
        .then(function(result) {
            console.log(result.results)
            app.recipes = result.results;
        })
    }
}

</script>
