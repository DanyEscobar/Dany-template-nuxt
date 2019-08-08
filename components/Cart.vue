<template>
  <div class="cart">
    <div class="container">
      <div class="row">
        <table class="shop-table">
          <thead>
            <tr>
              <th colspan="3" class="product-name">PRODUCT</th>
              <th class="product-quantity">QUANTITY</th>
              <th class="product-id">ID NUMBER</th>
              <th class="product-price">PRICE</th>
              <th class="product-subtotal">SUBTOTAL</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="product-remove">
                <a href="#" class="remove" title="Quitar este producto">
                  <img src="~/assets/images/remove.png" alt="Quitar producto">
                </a>
              </td>
              <td class="producto-image">
                <a href="#">
                  <img src="~/assets/images/item-1.jpg" alt="">
                </a>
              </td>
              <td class="product-info">
                <h2>Grey Striped Shirt</h2>
                <h4>T-shirt</h4>
              </td>
              <td class="product-quantity">
                <div>
                  <input type="number" step="1" min="0" max="99" name="cart" value="1" title="Qty" class="input-field"/>
                </div>
              </td>
              <td class="product-id">
                <span>AFN - 924222122</span>
              </td>
              <td class="product-price">
                <span>$49</span>
              </td>
              <td class="product-subtotal">
                <span>$49</span>
              </td>
            </tr>
            <tr>
              <td class="product-remove">
                <a href="#" class="remove" title="Quitar este producto">
                  <img src="~/assets/images/remove.png" alt="Quitar producto">
                </a>
              </td>
              <td class="producto-image">
                <a href="#">
                  <img src="~/assets/images/item-1.jpg" alt="">
                </a>
              </td>
              <td class="product-info">
                <h2>Grey Striped Shirt</h2>
                <h4>T-shirt</h4>
              </td>
              <td class="product-quantity">
                <div>
                  <input type="number" step="1" min="0" max="99" name="cart" value="1" title="Qty" class="input-field"/>
                </div>
              </td>
              <td class="product-id">
                <span>AFN - 924222122</span>
              </td>
              <td class="product-price">
                <span>$49</span>
              </td>
              <td class="product-subtotal">
                <span>$49</span>
              </td>
            </tr>
            <tr>
              <td class="product-remove">
                <a href="#" class="remove" title="Quitar este producto">
                  <img src="~/assets/images/remove.png" alt="Quitar producto">
                </a>
              </td>
              <td class="producto-image">
                <a href="#">
                  <img src="~/assets/images/item-1.jpg" alt="">
                </a>
              </td>
              <td class="product-info">
                <h2>Grey Striped Shirt</h2>
                <h4>T-shirt</h4>
              </td>
              <td class="product-quantity">
                <div>
                  <input type="number" step="1" min="0" max="99" name="cart" value="1" title="Qty" class="input-field"/>
                </div>
              </td>
              <td class="product-id">
                <span>AFN - 924222122</span>
              </td>
              <td class="product-price">
                <span>$49</span>
              </td>
              <td class="product-subtotal">
                <span>$49</span>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.cart {
  margin-bottom: 80px;
  padding: 40px;
}
.container {
  padding: 0;
  width: 750px;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}
.row {
  margin-right: -15px;
  margin-left: -15px;
}
tr {
  border: 1px solid #a8a8a8;
  border-collapse: collapse;
  margin: 0 0 35px;
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
thead, th {
  font-family: 'Montserrat Semi Bold';
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding: 18px 0;
  color: #000;
  text-align: left;
} 

.product-name {
  color: #000000;
  padding: 18px 0px 18px 172px;
}

.product-remove {
  font: 14px;
  padding: 10px 20px !important;
  
}
img {
  height: auto;
  max-width: 100%;
  margin: 35px 0px;
}
span {
  font-size: 12px;
  color: #404040;
  font-family: 'Montserrat Light';
  margin-left: 10px;
}


* {
  margin: 0;
  padding: 0;
}
body {
  background: #ffffff;
  word-wrap: break-word;
  overflow-x: hidden;
  font-family: "Open Sans", sans-serif;
  font-size: 14px;
  line-height: 1.45em;
  color: #454545;
}
h2 {
  font-size: 13px;
  margin-top: 0px;
  font-family: "Raleway", sans-serif;
  font-size: 15px;
  margin: 21px 0 11px;
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


</style>