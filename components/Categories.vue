<template>
  <section>
    <nav>
      <div class="categories-container">
        <h3 class="categories-title">Categories</h3>
        <div class="man" v-for="(nameCat, index) in dataName" :key="index">
          <h3 class="man-title">
            <span>{{nameCat.nameCat}}</span>
          </h3>
          <div class="man-container" >
            <ul class="man-ul">
              <li v-for="(man, index) in data" :key="index">
                <a href="" class="a-option">{{man.name}}
                  <span>{{man.amount}}</span>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          name: "Loungewear",
          amount: "(8)"
        },
        {
          name: "Oversized & Longline",
          amount: "(10)"
        },
        {
          name: "Polo Shirts",
          amount: "(30)"
        },
        {
          name: "Shirts",
          amount: "(41)"
        },
        {
          name: "Shorts",
          amount: "(31)"
        },
        {
          name: "Suits & Blazers",
          amount: "(16)"
        },
        {
          name: "Sunglasses",
          amount: "(12)"
        },
        {
          name: "Swimwear",
          amount: "(52)"
        },
        {
          name: "Trousers & Chinos",
          amount: "(31)"
        },
      ],
      dataName: [
        {nameCat: "Man"},
        {nameCat: "Woman"},
        {nameCat: "Kids"},
        {nameCat: "All Products"}
      ]
    }
  }
}
</script>

<style scoped>
nav {
  float: left;
  position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
  margin-right: 8%;
  width: 20%;
}
.categories-container {
  margin-bottom: 60px;
  width: 100%;
}
.categories-title {
  font-family: 'Montserrat Semi Bold';
  text-transform: uppercase;
  font-size: 13px;
  letter-spacing: 1px;
}
.man-title {
  background-color: transparent;
  border-bottom: 1px solid #a8a8a8;
  border-top: 0px solid #a8a8a8;
  border-left: 0px solid #a8a8a8;
  border-right: 0px solid #a8a8a8;
  margin: 26px 0 0px;
  padding: 0px 0 12px;
  font-family: "Montserrat", sans-serif;
  color: #202020;
  text-transform: uppercase;
  font-size: 11px;
}
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
.a-option > span {
  float: right;
}
</style>