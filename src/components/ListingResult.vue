<script setup>
  const props = defineProps({
    url: String,
    name: String,
    brand: String,
    price: Number,
    sponsored: Boolean,
    hasFinancing: Boolean,
    isNew: {
      type: Boolean,
      default: true
    },
    oldPrice: Number,
    thirdParty: String
  })
</script>

<template>
    <router-link :to="url" class="result">
      <div v-if="(isNew !== null) && !isNew" class="condition">Refurbished</div>
      <div class="image"></div>
      <span v-if="thirdParty" class="seller">Sold by <a>{{thirdParty}}</a><br/></span>
      <span class="name">
        <span class="brand">{{brand}}</span>
        {{name}}
      </span><br/>
      <span class="price">${{price}}</span><span v-if="oldPrice" class="old-price">${{oldPrice}}</span><span v-if="hasFinancing" class="monthly-option"><br/> or $20.99 per month</span><br/>
      <span v-if="sponsored" class="sponsored">Sponsored</span>
    </router-link>
</template>

<style scoped>
.result {
  width: 200px;
  border: 1px solid black;
  margin: 16px;
  padding: 16px;
  position: relative;
}
.seller {
  font-size: 0.6rem;
}
.condition {
  position: absolute;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 5px;
  padding-right: 5px;
  top: -15px;
  right: 8px;
  background-color: #ddd;
  font-weight: bold;
  font-style: italic;
}
.old-price {
  text-decoration: line-through;
  opacity: 0.5;
  margin-left: 5px;
}
.result .image {
  width: 100%;
  aspect-ratio: 1/1;
  border: 1px solid black;
  background-image: url('https://store.storeimages.cdn-apple.com/1/as-images.apple.com/is/iphone-card-40-17pro-202509_FMT_WHH?wid=508&hei=472&fmt=p-jpg&qlt=95&.v=WVVFRzUzVk1oblJhbW9PbGNSU25ja3doNjVzb1FWSTVwZWJJYThYTHlrNzQzbUlIR1RvazhDRHNOQlYvM3g2dFIwdkZSSnBZYjhOaHBpM2lkYTFBUEZHTmVoMWFVZloyU3lqdmZCOUFEeDF6K2N6UFd4K21VWHNnbWZBQ3hSanQ');
  background-size: cover;
}
.result .name {
  width: 100%;
  font-size: 1rem;
}
.result .name .brand {
  font-weight: bold;
}
.result .sponsored {
  font-style: italic;
  font-weight: light;
  font-size: 0.8rem;
  position: absolute;
  bottom: 0;
}
  .result .monthly-option {
    font-style: italic;
    opacity: 0.5;
  }
</style>
