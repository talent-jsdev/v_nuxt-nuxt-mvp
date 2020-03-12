<template>
    <section class="single-recipe">
        <h1>{{ recipe.title }}</h1>
        <div>
            <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p>{{ recipe.description }}</p>
    </section>
</template>

<script>
export default {
      asyncData(context) {
    //   return axios.get()
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Delicious Pizza",
              description: "This is really a delicious meal!", 
              thumbnail:
                "https://assets.bonappetit.com/photos/597f6564e85ce178131a6475/16:9/w_1200,c_limit/0817-murray-mancini-dried-tomato-pie.jpg"
            },
            {
              id: "2",
              title: "See Food Salad",
              previewText: "Very tasty indeed!",
              description: "This is really a delicious meal!", 
              thumbnail:
                "https://www.cdc.gov/features/salmonella-food/salmonella-food_456px.jpg"
            }
          ].find(el => el.id === context.params.id)
        });
      }, 1500);
    });
  }
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