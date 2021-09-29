<template>
  <div class="container">
    <div class="navbar-brand">
      <h1>YOUR SHOPPING CART</h1>
    </div>
    <div class="mobile-list grid">
      <div class="grid-item">
        <img src="./assets/mobile.jpg" alt="" class="img" />
      </div>
      <div class="data grid-item">
        <ul class="desc">
          <li class="mtitle">Motorola moto g5s</li>
          <li class="mdesc">Smartphone, Grey</li>
        </ul>
      </div>
      <div class="data grid-item">
        <ul class="right">
          <li class="qunt">1</li>
          <li class="price"><span>AED</span> <b>549</b></li>
        </ul>
      </div>
    </div>
    <div class="mobile-list grid">
      <div class="grid-item">
        <img src="./assets/mobile.jpg" alt="" class="img" />
      </div>
      <div class="data grid-item">
        <ul class="desc">
          <li class="mtitle">Nokia 8 smartphone LTE,</li>
          <li class="mdesc">Polished copper</li>
        </ul>
      </div>
      <div class="data grid-item">
        <ul class="right">
          <li class="qunt">1</li>
          <li class="price"><span>AED</span> <b>1,199</b></li>
        </ul>
      </div>
    </div>
    <div class="mobile-list flex1">
      <div class="">
        <img src="./assets/mobile.jpg" alt="" class="img" />
      </div>
      <div class="data1 grid-item1">
        <div class="message grid">
          <input v-on:click.prevent="increment" type="button" value="+"  class="but"/>
          <p class="display">{{ count }}</p>
          <input v-on:click.prevent="decrement" type="button" value="-"  class="but"/>
        </div>
      </div>
      <div class="data2 grid-item1">
        <div class="svg">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-x-lg"
            viewBox="0 0 16 16"
          >
            <path
              d="M1.293 1.293a1 1 0 0 1 1.414 0L8 6.586l5.293-5.293a1 1 0 1 1 1.414 1.414L9.414 8l5.293 5.293a1 1 0 0 1-1.414 1.414L8 9.414l-5.293 5.293a1 1 0 0 1-1.414-1.414L6.586 8 1.293 2.707a1 1 0 0 1 0-1.414z"
            />
          </svg>
        </div>
      </div>
    </div>
    <hr />
    <div class="grid1">
      <div class="grid-item1">
        <ul>
          <li>TOTAL</li>
        </ul>
      </div>
      <div class="grid-item1"></div>
      <div class="grid-item1 price1">
        <ul>
          <li class=""><span>AED</span> <b>4,927</b></li>
          <li>Price inclusive of VAT</li>
        </ul>
      </div>
    </div>
    <div class="button">
      <input type="button" value="PROCEED TO CHECKOUT" class="button1" />
    </div><br><br>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      if (this.count > 0) {
        this.count--;
      }
    },
  },
};
</script>

<style>
.but{
  font-size: 12vh;
}
.display {
  background-color: aliceblue;
  display: flex;
  align-items: center;
  border: 1px solid whitesmoke;
  justify-content: center;
  height: 20vh;
  font-size: 8vh;
}
.svg {
  display: inline-block;
  width: 120px;

  font-weight: bold;
}
.flex1 {
  display: flex;
  padding: 10px;
}
.data0 {
  width: 20em;
}
.container {
  background-color: rgba(200, 200, 200, 0.938);
}
svg {
  float: right;
  position: relative;
}
.navbar-brand {
  padding: 30px;
  font-weight: bold;
}
.mobile-list {
  background-color: white;
  margin: 20px;
}
.data {
  position: relative;
  float: right;
}
.grid {
  display: grid;
  grid-template-columns: auto auto auto;
  padding: 10px;
}
.grid-item {
  padding: 20px;
  text-align: left;
}
.grid1 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  padding: 10px;
}
.grid-item1 {
  padding: 20px;
  text-align: left;
}
ul {
  list-style-type: none;
}
.qunt {
  display: block;
  height: 60px;
  width: 60px;
  line-height: 60px;

  -moz-border-radius: 30px; /* or 50% */
  border-radius: 30px; /* or 50% */

  background-color: rgb(160, 160, 160);
  color: black;
  text-align: center;
  font-size: 2em;
}
span {
  color: rgba(160, 160, 160, 0.856);
}
.price {
  padding-top: 80px;
}
.img {
  padding: 15px;
  border: 1px solid green;
}
.mtitle {
  font-weight: bold;
  font-size: 4vh;
}
hr {
  border: 3px solid rgba(160, 160, 160, 0.856);
}
.price1 {
  font-size: 5vh;
}
.button {
  display: flex;
  justify-content: center;
}
.button1 {
  background-color: rgb(0, 172, 224);
  border: solid 2px rgb(0, 172, 213);
  display: inline-block;
  box-sizing: border-box;
  width: 80vh;
  height: 15vh;
  border-radius: 1em;
  font-weight: bold;
  color: whitesmoke;
  font-size: 5vh;
}
.data1 {
  background-color: rgba(49, 21, 21, 0.294);
  width: 150vh;
}
.data2 {
  background-color: rgba(230, 90, 90, 0.507);
  width: 55vh;
}
</style>
