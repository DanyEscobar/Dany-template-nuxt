<template>
  <section class="container">
    <div class="modal" v-if="modal1" @click="closeModal">
      <figure class="wrapper-img">
        <button title="Close" type="button" class="mfp-close" @click="closeModal">×</button>
        <img class="mfp-img" src="../assets/images/01.jpg" style="max-height: 1330px;" />
      </figure>
    </div>
    <div class="categories-container">
      <h3 class="categories-title">Categories</h3>
      {{$data.dataName[0].state}}A
      {{$data.state}}B
      <div class="man" v-for="(nameCat, index) in dataName" :key="index" @click="closeCategories">
        <h3 class="man-title">
          <span class="name-categorie">+</span>
          {{nameCat.nameCat}}
        </h3>
        <div class="man-container">
          <ul class="man-ul" v-if="state">
            <li v-for="(man, index) in data" :key="index">
              <a href="#" class="a-option">
                {{man.name}}
                <span>{{man.amount}}</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="cart-list">
      <cartList @mostrarModal="updateModal"></cartList>
    </div>
  </section>
</template>

<script>
import CartList from '../components/Cart-list'
export default {
  components: { CartList },
  data() {
    return {
      modal1: false,
      state: false,
      data: [
        {
          name: 'Loungewear',
          amount: '(8)'
        },
        {
          name: 'Oversized & Longline',
          amount: '(10)'
        },
        {
          name: 'Polo Shirts',
          amount: '(30)'
        },
        {
          name: 'Shirts',
          amount: '(41)'
        },
        {
          name: 'Shorts',
          amount: '(31)'
        },
        {
          name: 'Suits & Blazers',
          amount: '(16)'
        },
        {
          name: 'Sunglasses',
          amount: '(12)'
        },
        {
          name: 'Swimwear',
          amount: '(52)'
        },
        {
          name: 'Trousers & Chinos',
          amount: '(31)'
        }
      ],
      dataName: [
        { nameCat: 'Man', state: true },
        { nameCat: 'Woman', state: false },
        { nameCat: 'Kids', state: false },
        { nameCat: 'All Products', state: false }
      ]
    }
  },
  methods: {
    updateModal(newValue) {
      this.modal1 = newValue
    },
    closeModal() {
      this.modal1 = false
    },
    closeCategories() {
      this.state = true
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 1400px;
  width: 100%;
  margin-bottom: 80px;
  padding: 0px;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
  display: grid;
  grid-template-columns: 25% 1fr;
}
.modal {
  width: 100%;
  height: 100%;
  background-color: rgba(64, 64, 64, 0.667);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
}

.categories-container {
  margin-bottom: 60px;
  padding: 0 15px;
  max-width: 1200px;
  width: 100%;
  margin-right: auto;
  margin-left: auto;
  width: 100%;
}

/* .categories-container .man .man-container li a {
  color: #404040;
  font-size: 12px;
  display: block;
  padding: 10px 0 13px;
  -webkit-transform: all 0.2s ease 0s;
  -ms-transform: all 0.2s ease 0s;
  transform: all 0.2s ease 0s;
} */
.categories-title {
  font-family: 'Montserrat Semi Bold';
  text-transform: uppercase;
  font-size: 13px;
  letter-spacing: 1px;
  margin-bottom: 14px;
  border-bottom: 2px solid #d3d3d3;
  color: #292929;
  padding-bottom: 10px;
}
.man .man-title {
  background-color: transparent;
  border-bottom: 1px solid #a8a8a8;
  border-top: 0px solid #a8a8a8;
  border-left: 0px solid #a8a8a8;
  border-right: 0px solid #a8a8a8;
  margin: 26px 0 0px;
  padding: 0px 0 12px;
  font-family: 'Montserrat', sans-serif;
  color: #202020;
  text-transform: uppercase;
  font-size: 11px;
  cursor: pointer;
}
.name-categorie {
  background: url('../assets/images/plus.png') no-repeat scroll 0 0;
  float: right;
  padding-right: 10px;
  color: transparent;
}
/* .name-categorie {
  background: url('../assets/images/minas.png') no-repeat scroll 0 0;
} */
.man-container {
  padding: 6px 22px 6px 14px;
  border: 0px solid;
  border-bottom-right-radius: 3px;
  background: #ffffff;
  color: #333333;
}
.man-ul {
  list-style: none;
  padding: 0px;
  margin: 0px;
}
.a-option {
  background: #ffffff;
  color: #333333;
  color: #404040;
  font-size: 12px;
  display: block;
  padding: 10px 0 13px;
  text-decoration: none;
  outline: none;
}
.a-option:hover {
  color: #fda341;
}
.a-option > span {
  float: right;
}
img.mfp-img {
  width: 100%;
  display: block;
}
.wrapper-img {
  position: relative;
  max-width: 900px;
  width: 100%;
  height: auto;
  margin: 3% auto;
}
.mfp-close {
  position: absolute;
  top: -30px;
  right: 0;
  color: #fff;
  background: transparent;
  cursor: pointer;
  border: 0;
  font-size: 28px;
  font-family: Arial, Baskerville, monospace;
}

@media (min-width: 1200px) {
  .container {
    width: 750px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 970px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1250px;
  }
}
</style>