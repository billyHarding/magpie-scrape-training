<script setup>
  import ListingResult from '../../components/ListingResult.vue'
  const results = [
  {
    "url": "iphone-15-pro",
    "name": "iPhone 15 Pro",
    "price": 999.99,
    "brand": "Apple",
    "sponsored": true
  },
  {
    "url": "iphone-15",
    "name": "iPhone 15",
    "price": 799.99,
    "brand": "Apple",
    "sponsored": true
  },
  {
    "url": "samsung-galaxy-s24-ultra",
    "name": "Samsung Galaxy S24 Ultra",
    "price": 1199.99,
    "brand": "Samsung",
    "sponsored": true
  },
  {
    "url": "samsung-galaxy-s24",
    "name": "Samsung Galaxy S24",
    "price": 899.99,
    "brand": "Samsung",
    "sponsored": false
  },
  {
    "url": "google-pixel-8-pro",
    "name": "Google Pixel 8 Pro",
    "price": 999.0,
    "brand": "Google",
    "sponsored": false
  },
  {
    "url": "google-pixel-8",
    "name": "Google Pixel 8",
    "price": 699.0,
    "brand": "Google",
    "sponsored": false
  },
  {
    "url": "oneplus-12",
    "name": "OnePlus 12",
    "price": 799.0,
    "brand": "OnePlus",
    "sponsored": false
  },
  {
    "url": "oneplus-11",
    "name": "OnePlus 11",
    "price": 699.0,
    "brand": "OnePlus",
    "sponsored": false
  },
  {
    "url": "xiaomi-14-pro",
    "name": "Xiaomi 14 Pro",
    "price": 899.99,
    "brand": "Xiaomi",
    "sponsored": false
  },
  {
    "url": "xiaomi-13",
    "name": "Xiaomi 13",
    "price": 649.99,
    "brand": "Xiaomi",
    "sponsored": false
  },
  {
    "url": "sony-xperia-1-v",
    "name": "Sony Xperia 1 V",
    "price": 1099.99,
    "brand": "Sony",
    "sponsored": false
  },
  {
    "url": "sony-xperia-5-v",
    "name": "Sony Xperia 5 V",
    "price": 799.99,
    "brand": "Sony",
    "sponsored": false
  },
  {
    "url": "asus-rog-phone-8",
    "name": "ASUS ROG Phone 8",
    "price": 999.99,
    "brand": "ASUS",
    "sponsored": false
  },
  {
    "url": "samsung-galaxy-z-fold-5",
    "name": "Samsung Galaxy Z Fold 5",
    "price": 1799.99,
    "brand": "Samsung",
    "sponsored": false
  },
  {
    "url": "samsung-galaxy-z-flip-5",
    "name": "Samsung Galaxy Z Flip 5",
    "price": 999.99,
    "brand": "Samsung",
    "sponsored": false
  },
  {
    "url": "motorola-edge-40-pro",
    "name": "Motorola Edge 40 Pro",
    "price": 799.99,
    "brand": "Motorola",
    "sponsored": false
  },
  {
    "url": "nokia-x30",
    "name": "Nokia X30",
    "price": 529.99,
    "brand": "Nokia",
    "sponsored": false
  },
  {
    "url": "oppo-find-x6-pro",
    "name": "Oppo Find X6 Pro",
    "price": 899.99,
    "brand": "Oppo",
    "sponsored": false
  },
  {
    "url": "vivo-x100-pro",
    "name": "Vivo X100 Pro",
    "price": 849.99,
    "brand": "Vivo",
    "sponsored": false
  },
  {
    "url": "realme-gt-5",
    "name": "Realme GT 5",
    "price": 599.99,
    "brand": "Realme",
    "sponsored": false
  }
]
</script>

<template>
  <ListingResult v-for="result in results" v-bind="result"/>
</template>

<style scoped>
</style>
