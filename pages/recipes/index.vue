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
import Recipe from "@/components/Recipe";
export default {
  components: {
    Recipe
  },
  asyncData() {
    //   return axios.get()
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Delicious Pizza",
              previewText: "Delicious Pizza",
              thumbnail:
                "https://assets.bonappetit.com/photos/597f6564e85ce178131a6475/16:9/w_1200,c_limit/0817-murray-mancini-dried-tomato-pie.jpg"
            },
            {
              id: "2",
              title: "See Food Salad",
              previewText: "Very tasty indeed!",
              thumbnail:
                "https://www.cdc.gov/features/salmonella-food/salmonella-food_456px.jpg"
            }
          ]
        });
      }, 1500);
    });
  }
};
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
</style>