<template>
    <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
        <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.descriptionText }}</p>
    </section>
</template>

<script>
export default {
    asyncData(context) {
        return new Promise((resovle, reject) => {
            setTimeout(() => {
                resovle({
                    recipe:[
                        {
                            id: "1",
                            title: "Delicious Pizza",
                            previewText: "Awesome Pizza!",
                            descriptionText: "This is a really delicious pizza",
                            thumbnail: "https://miro.medium.com/max/5120/1*MfhIfzrC6x6T1-szQkjtCg.jpeg"
                        },
                        {
                            id: "2",
                            title: "Fresh Vegetables",
                            previewText: "Healthy Food!",
                            thumbnail: "https://www.healthyeating.org/images/default-source/home-0.0/nutrition-topics-2.0/general-nutrition-wellness/2-2-2-2foodgroups_vegetables_detailfeature.jpg?sfvrsn=226f1bc7_6"
                        },
                        {
                            id: "3",
                            title: "Italian Spagetti",
                            previewText: "Spagetti Carbonara",
                            descriptionText: "Taste the most delicious italian Spagetti!",
                            thumbnail: "https://www.budgetbytes.com/wp-content/uploads/2018/04/The-Best-Weeknight-Pasta-Sauce-plate-H1-480x270.jpg"
                        },
                    ].find(el => el.id === context.params.id)   
                })
            }, 1500)
        })
    },
}
</script>

<style scoped>
.single-recipe {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
}

.recipe-image {
    width: 100%;
}
</style>