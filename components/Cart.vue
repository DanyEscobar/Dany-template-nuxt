<template>
  <section>
    <div class="cart">
      <div class="container responsive">
        <div class="row">
          <table class="shop-table">
            <thead>
              <tr>
                <th colspan="3" class="product-name">Product</th>
                <th class="product-quantity">Quantity</th>
                <th class="product-id">Id number</th>
                <th class="product-price">Price</th>
                <th class="product-subtotal">Subtotal</th>
              </tr>
            </thead>
            <tbody>
              <tr class="cart-item" v-for="(item, index) in data" :key="index">
                <td class="product-remove">
                  <a
                    href="#"
                    class="remove"
                    title="Quitar este producto"
                    @click="removeProduct(index)"
                  >
                    <img :src="item.remove" alt="Quitar producto" />
                  </a>
                </td>
                <td class="product-image">
                  <a href="#">
                    <img :src="item.thumbnail" class="image-nor"/>
                  </a>
                </td>
                <td class="product-info">
                  <h2>{{item.name}}</h2>
                  <h4>{{item.info}}</h4>
                </td>
                <td class="product-quantity">
                  <div class="input-quantity">
                    <input
                      type="number"
                      step="1"
                      min="0"
                      max="99"
                      name="cart"
                      :value="item.quantity"
                      title="Qty"
                      class="input-field"
                    />
                  </div>
                </td>
                <td class="product-id">
                  <span>{{item.id}}</span>
                </td>
                <td class="product-price">
                  <span>{{item.price}}</span>
                </td>
                <td class="product-subtotal">
                  <span>{{item.subtotal}}</span>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      <div class="version-responsive">
        <div class="cart-responsive">
          <h5 class="cart-title">
            Your shopping cart
            <span>({{data.length}} items)</span>
          </h5>
          <br />
          <div class="table">
            <div class="product-cart" v-for="(item, index) in data" :key="index">
              <div class="cart-product-remove">
                <a
                  href="#"
                  class="cart-remove"
                  title="Quitar este producto"
                  @click="removeProduct(index)"
                >
                  <img class="image-responsive-remove" :src="item.remove" alt="Quitar producto" />
                </a>
              </div>
              <div class="cart-product-image">
                <a href="#" class="a-responsive">
                  <img class="image-responsive" :src="item.thumbnail" />
                </a>
              </div>
              <div class="cart-product-info">
                <h5>{{item.name}}</h5>
                <span>
                  <h6>{{item.info}}</h6>
                </span>
                <div class="cart-product-price">
                  <del>$80</del>
                  "{{item.price}}"
                </div>
                <div class="cart-product-delete">
                  <button class="product-delete" @click="removeProduct(index)">Delete</button>
                </div>
              </div>
            </div>
            <div class="order-total">
              <h5 class="title-order">Order total</h5>
            </div>
            <div class="checkout">
              <h4 class="total-price">
                <span class="amount">$166</span>
              </h4>
              <button class="cart-checkout">Checkout</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          remove: require('~/assets/images/remove.png'),
          thumbnail: require('~/assets/images/item-1.jpg'),
          name: 'Grey Striped Shirt1',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$49',
          subtotal: '$49'
        },
        {
          remove: require('~/assets/images/remove.png'),
          thumbnail: require('~/assets/images/item-1.jpg'),
          name: 'Grey Striped Shirt2',
          info: 'T-shir',
          quantity: 2,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        },
        {
          remove: require('~/assets/images/remove.png'),
          thumbnail: require('~/assets/images/item-1.jpg'),
          name: 'Grey Striped Shirt3',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48'
        }
      ]
    }
  },
  methods: {
    removeProduct(i) {
      this.data.splice(i, 1)
    }
  }
}
</script>

<style scoped>
/* cart */
* {
  margin: 0;
  padding: 0;
}

.cart {
  margin-bottom: 80px;
  padding: 40px;
}

.container {
  padding: 0;
  max-width: 1200px;
  width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}

.row {
  margin-right: -15px;
  margin-left: -15px;
  font: 14px 'Open Sans', sans-serif;
  color: #454545;
}

tr {
  border: 1px solid #a8a8a8;
  border-collapse: collapse;
  margin: 18px 0px;
}

table {
  margin: 0 0 1.5em;
  width: 100%;
  border: 1px solid #a8a8a8;
  background-color: transparent;
  border-spacing: 0;
  border-collapse: collapse;
  display: table;
  margin: 0 0 35px;
}

.cart .shop-table thead,
th {
  font-family: 'Monserrat', sans-serif;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 18px 0px;
  color: #000;
  text-align: left;
  font-weight: bold;
}

td.product-remove {
  padding: 10px 20px;
  font: 14px 'Open Sans', sans-serif;
  color: #454545;
  text-align: center;
  width: 9%;
}
td.product-remove a {
  /* width: 100%; */
  display: flex;
  justify-content: center;
  /* align-items: center; */
}
td.product-image {
  width: 100px;
  /* width: 9.5%; */
  /* height: 100%; */
  display: flex;
  /* justify-content: center; */
  /* align-items: center; */
}
td.product-image a {
  /* width: 100%; */
  display: flex;
  justify-content: center;
  /* align-items: center; */
}
td.product-image img {
  width: 74px;
  margin: 35px 0;
}

th.product-name {
  color: #000000;
  padding-left: 20%;
}

td.product-info {
  width: 25.7%;
  color: #454545;
  font: 14px 'Open Sans', sans-serif;
}
h2 {
  font-size: 13px;
  margin-top: 0px;
  font-family: 'Raleway', sans-serif;
  margin: 0px 0px 11px;
  color: #292929;
  letter-spacing: 1px;
  text-transform: capitalize;
  font-weight: 500;
  margin-block-start: 0.83em;
  margin-block-end: 0.83em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  display: block;
}
h4 {
  font-size: 11px;
  color: #878787;
  letter-spacing: 1px;
  font: 12px 'Raleway', sans-serif;
}

td.product-quantity {
  width: 14.8%;
  color: #454545;
  font: 14px 'Open Sans', sans-serif;
}
td.product-quantity input {
  width: 63px;
  padding: 13px 0 11px 15px;
  border: 1px solid #a8a8a8;
  margin: 15px 0px 30px;
  font: 14px 'Open Sans', sans-serif;
}

td.product-id {
  width: 17%;
  font: 14px 'Open Sans', sans-serif;
  color: #454545;
}

td.product-price {
  width: 14%;
  font: 14px 'Open Sans', sans-serif;
  color: #454545;
}
span {
  font: 14px 'Open Sans', sans-serif;
  color: #454545;
}

td.product-subtotal {
  width: 11%;
  font: 14px 'Open Sans', sans-serif;
}
td.product-subtotal span {
  color: #202020;
  font: 14px 'Open Sans', sans-serif;
}

.imgage-nor {
  height: auto;
  max-width: 100%;
}

body {
  background: #ffffff;
  word-wrap: break-word;
  overflow-x: hidden;
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  line-height: 1.45em;
  color: #454545;
}
.version-responsive {
  display: none;
}
@media (max-width: 1200px) {
  .container {
    max-width: 1170px;
  }
}
@media (max-width: 730px) {
  .responsive {
    display: none;
  }
  .version-responsive {
    display: initial;
  }
  .cart {
    padding: 0;
  }
}


/* Cart Responsive */

.cart-responsive {
  min-width: 100%;
  height: auto;
  background-color: #fff;
  padding: 20px;
  padding-top: 20px;
  /* box-shadow: 2px 5px 10px #ddd; */
  top: 50px;
  right: 50px;
}
.table {
  border: 1px solid #a8a8a8;
  border-collapse: collapse;
  width: 100%;
  display: table;
}
.product-cart {
  display: flex;
  /* justify-content: space-around; */
  align-items: center;
  border-bottom: 1px solid #999999;
  padding: 10px;
  padding-bottom: 40px;
  padding-top: 40px;
  width: 100%;
}
.cart-product-remove {
  width: 20%;
}
.cart-remove  {
  justify-content: center;
  display: flex;
  align-items: center; 
}
.image-responsive-remove{
  align-items: center;
  align-content: center;
}
.cart-product-image {
  flex: 1;
  width: 33%;
}
.a-responsive {
  width: 100%;
  display: flex;
}
.image-responsive{
  width: auto;
}
.cart-product-info {
  width: 34%;
  text-align: left;
  flex: 1;
}
h5 {
  color: #292929;
  font-size: 13px;
  font-family: 'Raleway', sans-serif;
  font-weight: 600;
}
.cart-product-delete {
  text-align: left;
  flex: 1;
}
.product-delete {
  color: #000;
  margin-top: 10px;
}
button {
  font-weight: lighter;
  display: inline-block;
  margin-top: 10px;
  padding: 10px 18px;
  background: none;
  border-radius: 0px;
  border: 1px solid #a8a8a8;
  font-family: 'Montserrat Light';
  font-size: 13px;
  text-align: center;
  background-color: transparent;
}
button:hover {
  width: auto;
  height: auto;
  background-color: #fda341;
  color: #ffffff;
  border: 1px solid #fda341;
  transform: scale(0.9999);
  transition: transform 0.35s;
}
.order-total {
  padding-left: 10px;
  padding-top: 10px;
  margin: 10px 0;
}
.title-order {
  color: #292929;
}
.checkout {
  padding: 10px 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cart-checkout {
  color: #000;
  margin-top: -15px;
}
.total-price {
  width: auto;
  height: auto;
  color: #000;
  font-size: 14px;
}

</style>