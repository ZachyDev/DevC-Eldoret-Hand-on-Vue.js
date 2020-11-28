<template>
  <div class="products">
    <div class="jumbotron">
    <h1>{{ title }}</h1>
    <button type="button" class="btn btn-primary" id="btn">Cart <span class="badge badge-warning">{{ items }}</span></button>
  </div>
  <div class="product__details">

  <!-- product one start-->
    <div id="product__one">
      <img src="@/assets/prod1.jpg" alt="product 1">
      <div id="desc">
          <p>Apple MacBook Pro 13</p>
      </div>
      <span id="product__info">
        KSH20000
      </span>
      <div id="addToCart">
        <button type="button" class="btn btn-warning" id="addBtn" @click="addToCart">Add to cart</button>
      </div>

    </div>
  <!-- product one end-->

       <!-- product two start-->
    <div id="product__two">
      <img src="@/assets/prod2.jpg" alt="product 1">
        <div id="desc">
          <p>Apple MacBook Pro 13</p>
      </div>
       <span id="product__info">
        KSH20000
      </span>
       <div id="addToCart">
       <button type="button" class="btn btn-warning" id="addBtn" @click="addToCart">Add to cart</button>
      </div>
    </div>
    <!-- product two end-->

   <!-- product three start-->
    <div id="product__three">
      <img src="@/assets/prod3.jpg" alt="product 1">
        <div id="desc">
          <p>Apple MacBook Pro 13</p>
      </div>
       <span id="product__info">
        KSH20000
      </span>
       <div id="addToCart">
        <button type="button" class="btn btn-warning" id="addBtn" @click="addToCart">Add to cart</button>
      </div>
    </div>
  </div>
  <!-- product three end -->

</div>
</template>

<script>
export default {
  name: 'Products',
  data() {
    return {
      items: 0,
      title: "DevC Eldoret Hands on Vue.js",
      addProduct: '',
      products: [],
    }
  },
  methods: {
    addToCart() {
        this.items += 1;
    },
    addStock() {
      this.products.push(this.addProduct)
    }
  }
}
</script>

<style scoped>
  .jumbotron {
    display: flex;
    justify-content: space-between;
  }
  #btn {
    width: 100px;
    height: 40px;
  }
  .product__details {
    display: flex;
    justify-content: space-around;
  }
  #product__info {
    display: flex;
    justify-content: space-around;
  }
  #desc {
    display: flex;
    justify-content: center;
  }
  #addToCart {
    display: flex;
    justify-content: center;
    margin-top: 20px;
  }
  #addBtn {
    display: flex;
    text-transform: uppercase;
    color: #fff;
    font-family: Helvetica, sans-serif;
    font-weight: bold;
    font-size: 17px;
    background-color: #f68b1e;
  }
  @media(max-width:789px) {
    .jumbotron {
      display: flex;
      flex-direction: column;
      width: 100%;
      height: auto;
    }
    .product__details {
      display: flex;
      flex-direction: column;
    }
  }
</style>