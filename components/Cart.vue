<template>
  <div class="cart">
    <div class="container">
      <table class="shop-table">
        <thead>
          <tr>
            <th class="product-name">PRODUCT</th>
            <th class="product-quantity">QUANTITY</th>
            <th class="product-id">ID NUMBER</th>
            <th class="product-price">PRICE</th>
            <th class="product-subtotal">SUBTOTAL</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="remove">
              <h4>Grey Striped Shirt</h4>
              <h5>T-shirt</h5>
            </td>
            <td>
              <div>
                <input type="number" min="0" max="100" />
              </div>
            </td>
            <td>AFN - 924222122</td>
            <td>$49</td>
            <td>$49</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
table,
tbody,
thead,
tr {
  border: 1px solid grey;
  border-collapse: collapse;
}
th,
td {
  text-align: center;
}
.cart {
  padding: 20px;
}
.cart .shop-table thead th {
  font-family: Montserrat Semi Bold;
}
</style>