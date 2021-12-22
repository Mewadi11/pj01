<template>
  <div class="center_box">
    <div class="col">
      <div class="buttoncreate">
        <b-button href="#" variant="primary" @click="catcreate"
          >สร้าง category</b-button
        >
      </div>
      <div class="catrgory_grid">
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่1</div>
        </a>
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่2</div>
        </a>
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่3</div>
        </a>
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่4</div>
        </a>
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่5</div>
        </a>
        <a href="#" class="category_item">
          <div class="category__text">หมวดหมู่6</div>
        </a>
      </div>
    </div>

    <div class="parent ml-x">
      <div class="box">
        <div class="boxcategory"></div>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  layout: "user",
  data() {
    return {
      name: "",
      lastname: "",
    };
  },
  methods: {
    catcreate() {
      this.$router.push("category/catcreate");
    },
  },
};
</script>

<style scoped>
.center_box {
  flex-grow: 1;
  display: flex;
  padding-left: 50px;
  padding-right: 50px;
}
.buttoncreate {
  margin-top: 30px;
  text-align: center;
  justify-content: flex-end;
  display: flex;
}
.parent {
  display: flex;
  flex-wrap: wrap;
}
.box {
  width: 100%;
}
.boxcategory {
  background-color: rgb(231, 12, 12);
}
.catrgory_grid {
  border: 5px solid black;
  background-color: rgb(50, 8, 90);
  margin-top: 100px;
  min-height: 70vh;
  display: flex;
  grid-template-columns: 1fr 1fr 1fr;
  flex-wrap: wrap;
}
.category_item {
  /* box-shadow: 0px 3px 12px rgb(0 0 0 / 15%);
  transition: all 100ms ease-in-out; */
  border-radius: 0.3125rem;
  border: 5px solid black;
  flex-wrap: wrap;
  margin: 20px;
  background-color: rgb(255, 178, 36);
  width: 200px;
  /* margin-bottom: 50px;
  margin-right: 20px;
  margin-left: 20px;
  margin-top: 20px; */
  height: 12.5rem;
  align-content: 0 0 calc(33% / 3);
}

.category__text {
  font-size: 14px;
  color: #000;
  text-align: center;
  height: 100%;
  text-justify: inherit;
}
</style>