<template>
  <div class="cart-item-list">
    <div class="item-list" v-for="(item, index) in data" :key="index">
      <div class="single-item-list">
        <div class="cart-product-image">
          <img class="image-responsive" :src="item.thumbnail" />
        </div>
        <div class="product-info">
          <h2>{{item.name}}</h2>
          <h4 class="product-name">{{item.info}}</h4>
          <div class="price">
            {{item.price}}
            <del>$50</del>
          </div>
          <div class="entry-content">
            <p>{{item.content}}</p>
          </div>
          <div class="actions">
            <ul>
              <li>
                <a class="add-cart" href="#" @click="addProduct(item)">
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
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          thumbnail: require('~/assets/images/01.jpg'),
          name: 'Grey Striped Shirt1',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$49',
          subtotal: '$49',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        },
        {
          thumbnail: require('~/assets/images/02.jpg'),
          name: 'Grey Striped Shirt2',
          info: 'T-shir',
          quantity: 2,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        },
        {
          thumbnail: require('~/assets/images/03.jpg'),
          name: 'Grey Striped Shirt3',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        },
        {
          thumbnail: require('~/assets/images/04.jpg'),
          name: 'Grey Striped Shirt4',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        },
        {
          thumbnail: require('~/assets/images/05.jpg'),
          name: 'Grey Striped Shirt5',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        },
        {
          thumbnail: require('~/assets/images/06.jpg'),
          name: 'Grey Striped Shirt6',
          info: 'T-shir',
          quantity: 1,
          id: 'AFN - 924222122',
          price: '$48',
          subtotal: '$48',
          content:
            'Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.image-responsive {
  width: 100%;
  height: inherit;
  display: block;
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
.single-item-list {
  display: flex;
  padding: 0px 15px 45px;
  width: 100%;
}
.single-item-list .cart-product-image {
  padding: 0px 12px 0px 0px;
  width: 33.33333333%;
  height: inherit;
}
.single-item-list .cart-product-image .image-responsive {
  width: 100%;
  height: inherit;
}

.single-item-list .product-info {
  width: 66.66666667%;
  margin: 0px 0px 0px 18px;
  padding: 40px 0px 0px;
}
.single-item-list .product-info h2 {
  font-family: 'Raleway', sans-serif;
  font-size: 15px;
  margin: -4px 0 10px;
  color: #292929;
  letter-spacing: 1px;
  text-transform: capitalize;
  font-weight: 500;
}
.single-item-list .product-info .product-name {
  font-size: 14px;
  color: #878787;
  text-transform: capitalize;
  margin-bottom: 13px;
  font-family: 'Raleway', sans-serif;
  clear: both;
  line-height: 1.4em;
  -webkit-font-smoothing: antialiased;
}
.single-item-list .price {
  margin-bottom: 13px;
  font-size: 14px;
  font-family: 'Montserrat', sans-serif;
  color: #fda341;
  letter-spacing: 1px;
  font-weight: 300;
}
.single-item-list .price del {
  color: #878787;
  margin-left: 25px;
  margin-right: 0;
  font-weight: 300;
  font-family: 'Montserrat', sans-serif;
  font-size: 13px;
}
.single-item-list .actions ul {
  margin: 0px;
  padding: 0px;
  list-style: none;
}
.single-item-list .actions ul li {
  display: inline;
  margin-right: 12px;
}
.single-item-list .actions ul li a.add-cart {
  padding: 13px 18px !important;
  font-family: 'Montserrat', sans-serif;
}
.single-item-list .actions ul li a.add-cart span {
  margin-right: 5px;
}
.single-item-list .actions ul li a {
  border: 1px solid #a8a8a8;
  display: inline-block;
  font-size: 10px;
  padding: 13px 13px;
  text-transform: uppercase;
  color: #5f5f5f;
}

p {
  margin-bottom: 20px;
  line-height: 30px;
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
a,
a:hover,
a:focus {
  text-decoration: none;
  outline: none;
}
a:hover {
  width: auto;
  height: auto;
  background-color: #fda341;
  color: #ffffff;
  border: 1px solid #fda341;
  transform: scale(0.9999);
  transition: transform 0.35s;
}
</style>