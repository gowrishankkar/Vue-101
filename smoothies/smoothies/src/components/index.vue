<template>
  <div class="index container">
    <div class="card" v-for="smoothie in smoothies" :key="smoothie.id">
      <div class="card-content">
        <h2 class="indigo-text">{{smoothie.title}}</h2>
        <ul class="ingredients">
          <li v-for="(ing, index) in smoothie.ingredients" :key="index">
            <span class="chip">{{ing}}</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      smoothies: [
        {title: 'cofee', slug: 'brew', ingredients: ['banana', 'tea', 'buiscut' ], id:1},
        {title: 'tea', slug: '3 roses', ingredients: ['milk', 'sugar', 'water' ], id:2},
      ]
    }
  }
}
</script>


<style >
  .index {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 30px;
    margin-top: 60px;
  }

  .index h2{
    font-size: 1.8rm;
    text-align: center;
    margin-top: 0;
  }

  .index .ingredients {
    margin: 30px auto;
  }

  .index .ingredients li{
    display: inline-block;
  }
</style>
