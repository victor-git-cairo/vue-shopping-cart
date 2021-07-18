<template>
  <div id="app">
     <h1>The Cup Store</h1>
            
            <product v-for="product in products" :key="product.key" :product="product"></product>
            
            <cart></cart>
  </div>
</template>

<script>
import Cart from './components/Cart';
import Product from './components/Product';

export default {
  name: 'App',
  data(){
    return {
     products:[
       {id: 100, name:"Colorful Cups",price:"999",image:"images/cups1.jpg"},
       {id: 101, name:"Coffee & Home",price:"1499",image:"images/cups2.jpg"},
       {id: 102, name:"Old Red Friend",price:"1999",image:"images/cups3.jpg"},
     ]
    }
  },
  components: {
    Product,
    Cart
  }
}
</script>

<style src="@/assets/styles.css">

</style>
