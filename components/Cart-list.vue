<template>
  <section>
    <div class="contenedor">
      {{$data.mostrar}}
      <div class="view-navigation">
        <div class="info-text">
          <p>Showing 1-1 from {{data1.length}} products</p>
        </div>
        <div class="right-content">
          <div class="grid-list">
            <ul>
              <li>
                <a href="#" @click="mostrar=true">
                  <i class="fa fa-align-justify"></i>
                </a>
              </li>
              <li class="active">
                <a href="#" class="active" @click="mostrar=false">
                  <i class="fa fa-th"></i>
                </a>
              </li>
            </ul>
          </div>
          <div class="input-select">
            <select name="sorted" id="sorted">
              <option value="-1">default sorting</option>
              <option>Price</option>
              <option>Useless</option>
              <option>Important</option>
            </select>
          </div>
        </div>
      </div>
      <div class="cart-item">
        <div class="item" v-for="(item, index) in data1" :key="index">
          <div class="single-item">
            <div class="cart-product-image">
              <img class="image-responsive" :src="item.thumbnail" />
              <div class="actions">
                <ul>
                  <li>
                    <a class="add-cart" href="#">
                      <span>
                        <span class="icon_plus"></span>
                      </span> add to cart
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <span class="icon_heart_alt"></span>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <span class="arrow_expand"></span>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="product-info">
              <h2>{{item.name}}</h2>
              <h4 class="product-name">{{item.info}}</h4>
              <div class="price">
                {{item.price}}
                <del>$50</del>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="cart-item-list" v-if="mostrar">
        <cartItemList></cartItemList>
      </div>
    </div>
  </section>
</template>

<script>
import CartItemList from '../components/Cart-item-list'
export default {
  components: { CartItemList },
  data() {
    return {
      mostrar: false,
      data1: [
        {
          thumbnail: require('~/assets/images/01.jpg'),
          name: 'Grey Striped Shirt1',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$49',
          subtotal: '$49'
        },
        {
          thumbnail: require('~/assets/images/02.jpg'),
          name: 'Grey Striped Shirt2',
          info: 'T-shir',
          quantity: 2,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
        {
          thumbnail: require('~/assets/images/03.jpg'),
          name: 'Grey Striped Shirt3',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
        {
          thumbnail: require('~/assets/images/04.jpg'),
          name: 'Grey Striped Shirt4',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
        {
          thumbnail: require('~/assets/images/05.jpg'),
          name: 'Grey Striped Shirt5',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
        {
          thumbnail: require('~/assets/images/06.jpg'),
          name: 'Grey Striped Shirt6',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
      ]
    }
  },
  methods: {
    mostrarVista() {
      this.$emit('click', this.mostrar != false)
    }
  }
}
</script>

<style scoped>
.contenedor {
}
.view-navigation {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  padding: 0px 15px;
  margin: 0 0 30px;
  align-items: center;
}
.view-navigation .info-text {
  display: block;
  float: left;
}
p {
  margin-bottom: 20px;
  line-height: 30px;
  margin: 0 0 10px;
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
}
.view-navigation .right-content {
  text-align: right;
}
.view-navigation .right-content .grid-list {
  display: inline-block;
}
.view-navigation .right-content .grid-list ul {
  margin: 0px;
  padding: 0px;
  list-style: none;
}
.view-navigation .right-content .grid-list ul li {
  display: inline-block;
  margin: 0 5px;
}
.view-navigation .right-content .grid-list ul li a {
  background-color: transparent;
  border: 1px solid #a8a8a8;
  color: #878787;
  display: inline-block;
  font-size: 20px;
  height: 41px;
  line-height: 36px;
  text-align: center;
  width: 40px;
}
a,
a:hover,
a:focus {
  text-decoration: none;
  outline: none;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
i {
  color: inherit;
}
.fa-align-justify:before {
  content: '\f039';
}
:after,
:before {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
.view-navigation .right-content .grid-list ul li a.active,
.view-navigation .right-content .grid-list ul li a:hover {
  color: #fda341;
}
.fa-th:before {
  content: '\f00a';
}
:after,
:before {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
.view-navigation .right-content .input-select {
  display: inline-block;
  float: right;
  position: relative;
}
.view-navigation .right-content .input-select select {
  -moz-appearance: none;
  background-color: transparent;
  border: 1px solid #a8a8a8;
  color: #878787;
  cursor: pointer;
  font-family: 'Montserrat Light';
  font-size: 10px;
  height: 41px;
  margin-left: 8px;
  outline: medium none;
  padding: 2px 7px 3px 7px;
  text-transform: uppercase;
  width: 180px;
}
.view-navigation .right-content .input-select select option {
  padding: 8px 5px;
  color: #555555;
}
/* .right-content {
  display: flex;
  justify-content: flex-end;
} */
.cart-item {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.item {
  display: flex;
  justify-content: center;
  color: #454545;
  font: 14px 'Open Sans', sans-serif;
  padding: 0px 15px;
}
.single-item {
  filter: alpha(opacity=0);
  filter: alpha(opacity=100);
  padding-bottom: 48px;
}
.single-item .cart-product-image {
  filter: alpha(opacity=0);
  filter: alpha(opacity=100);
  height: auto;
  position: relative;
}
.image-responsive {
  width: 100%;
  height: inherit;
  display: block;
}
.single-item .cart-product-image:hover .actions {
  bottom: -1px;
  opacity: 1;
  filter: alpha(opacity=100);
  -webkit-transform: scale(1);
  -ms-transform: scale(1);
  transform: scale(1);
}
.single-item .cart-product-image .actions {
  position: absolute;
  bottom: -8px;
  width: 100%;
  -webkit-transition: -webkit-transform 0.25s, opacity 0.15s, bottom 0.2s;
  transition: transform 0.25s, opacity 0.15s, bottom 0.2s;
  -webkit-transform: scale(0.5);
  -ms-transform: scale(0.5);
  transform: scale(0.8);
  opacity: 0;
  filter: alpha(opacity=0);
  background-color: #202020;
}
.single-item .cart-product-image .actions ul {
  margin: 0px;
  padding: 0px;
  list-style: none;
  overflow: hidden;
  /* padding: 15px 0; */
}
.single-item .cart-product-image .actions ul li:first-child {
  width: 64%;
}
.single-item .cart-product-image .actions ul li {
  width: 18%;
  float: left;
  text-align: center;
}
.single-item .cart-product-image .actions ul li a.add-cart {
  text-transform: uppercase;
  color: #ffffff;
  font-size: 10px;
  font-family: 'Montserrat', sans-serif;
  letter-spacing: 1px;
  text-decoration: none;
  outline: none;
}
.single-item .cart-product-image .actions ul li a {
  display: block;
  padding: 15px 0;
}
.single-item .cart-product-image .actions ul li a:hover {
  background-color: #323232;
}
.single-item .cart-product-image .actions ul li a.add-cart span {
  height: 15px;
}
.single-item .cart-product-image .actions ul li a span {
  color: #cacaca;
  font-size: 13px;
}
.single-item .cart-product-image .actions ul li a.add-cart span span {
  color: #ffffff;
  vertical-align: middle;
  display: inline-block;
}
.single-item .cart-product-image .actions ul li a.add-cart span {
  height: 15px;
}
.single-item .cart-product-image .actions ul li a span {
  color: #cacaca;
  font-size: 13px;
}
.icon_plus {
  font-family: 'ElegantIcons';
  speak: none;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
}
.icon_plus:before {
  content: '\4c';
}
:after,
:before {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
/* .actions ul li {
  width: 64%;
  float: left;
  text-align: center;
} */
.single-item .product-info {
  text-align: left;
}
.single-item .product-info h2 {
  font-family: 'Raleway', sans-serif;
  font-size: 15px;
  margin: 21px 0 11px;
  color: #292929;
  letter-spacing: 1px;
  text-transform: capitalize;
  font-weight: 500;
}
.single-item .product-name {
  font-size: 14px;
  color: #878787;
  text-transform: capitalize;
  margin-bottom: 13px;
  font-family: 'Raleway', sans-serif;
}
.single-item .price {
  font-size: 14px;
  font-family: 'Montserrat', sans-serif;
  color: #fda341;
  letter-spacing: 1px;
  font-weight: 300;
}
.single-item .price del {
  color: #cbcbcb;
  margin-left: 25px;
  margin-right: 0;
  font-weight: 300;
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
}
.icon_heart_alt {
  font-family: 'ElegantIcons';
  speak: none;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
}
.arrow_expand {
  font-family: 'ElegantIcons';
  speak: none;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
}
</style>