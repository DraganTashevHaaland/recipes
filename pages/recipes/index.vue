<template>
    <section class="recipes">
        <Recipe 
            v-for="recipe in recipes"
            :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText"
        />
    </section>
</template>

<script>
import Recipe from '@/components/Recipe';
export default {
    components: {
        Recipe
    },
    asyncData(context ) {
        return new Promise((resovle, reject) => {
            setTimeout(() => {
                resovle({
                    recipes: [
                        {
                            id: "1",
                            title: "Delicious Pizza",
                            previewText: "Awesome Pizza!",
                            thumbnail: "https://miro.medium.com/max/5120/1*MfhIfzrC6x6T1-szQkjtCg.jpeg"
                        },
                        {
                            id: "2",
                            title: "Fresh Vegetables",
                            previewText: "Healthy Food!",
                            thumbnail: "https://www.healthyeating.org/images/default-source/home-0.0/nutrition-topics-2.0/general-nutrition-wellness/2-2-2-2foodgroups_vegetables_detailfeature.jpg?sfvrsn=226f1bc7_6"
                        }
                    ]
                })
            }, 1500)
        })
    },
}
</script>

<style scoped>
.recipes {
    display: flex;
    flex-flow: row;
    justify-content: center;
    align-items: center;
}

</style>>

