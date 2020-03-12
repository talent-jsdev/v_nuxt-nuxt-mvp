<template>
  <section class="recipes">
    <article class="recipe">
      <div
        class="thumbnail"
        style="background-image: url('https://assets.bonappetit.com/photos/597f6564e85ce178131a6475/16:9/w_1200,c_limit/0817-murray-mancini-dried-tomato-pie.jpg')"
      ></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </article>
    <article class="recipe">
      <div
        class="thumbnail"
        style="background-image: url('https://www.cdc.gov/features/salmonella-food/salmonella-food_456px.jpg')"
      ></div>
      <h1>Title</h1>
      <p>Some nice preview text</p>
    </article>
  </section>
</template>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
  margin: 10px;
}

.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>