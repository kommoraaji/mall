<template>
  <div class="main">
    <v-title></v-title>

    <van-tree-select :items="items" :main-active-index.sync="active">
      <template #content>
        <div class="main" v-if="active === 0">
          <div class="stamp">
            <h1 class="tit">
              洗发类
              <span class="more">更多></span>
            </h1>
            <ul>
              <li class="shampoo" v-for="item in shampoo" :key="item.id">
                <img v-lazy="item.img" />
                <p>{{item.name}}</p>
              </li>
            </ul>
          </div>
          <div class="stamp">
            <h1 class="title">
              染发类
              <span class="mored">更多></span>
            </h1>
            <ul>
              <li class="shampoo" v-for="item in coloring" :key="item.id">
                <img v-lazy="item.img" />
                <p>{{item.name}}</p>
              </li>
            </ul>
          </div>
        </div>
      </template>
    </van-tree-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: 0,
      items: [
        { text: "施华寇" },
        { text: "沙宣" },
        { text: "欧莱雅" },
        { text: "潘婷" },
        { text: "资生堂" },
        { text: "阿道夫" },
        { text: "卡诗" },
        { text: "海飞丝" },
        { text: "资生堂" }
      ],
      shampoo: [
        {
          id: 1,
          name: "护亮泽洗发水",
          img: require("../../assets/images/sp01.jpg")
        },
        {
          id: 2,
          name: "滋养洗发水",
          img: require("../../assets/images/sp02.jpg")
        },
        {
          id: 3,
          name: "柔顺洗发露",
          img: require("../../assets/images/sp03.jpg")
        },
        {
          id: 4,
          name: "去屑洗发露",
          img: require("../../assets/images/sp04.jpg")
        },
        {
          id: 5,
          name: "柔顺洗发露",
          img: require("../../assets/images/sp05.jpg")
        },
        {
          id: 6,
          name: "焕彩洗发水",
          img: require("../../assets/images/sp06.jpg")
        }
      ],
      coloring: [
        {
          id: 7,
          name: "施华蔻染色",
          img: require("../../assets/images/sp07.jpg")
        },
        {
          id: 8,
          name: "施华蔻双氧乳",
          img: require("../../assets/images/sp08.jpg")
        },
        {
          id: 9,
          name: "施华蔻染发膏",
          img: require("../../assets/images/sp09.jpg")
        }
      ]
    };
  },
  methods: {},
  mounted() {}
};
</script>
<style lang="" scoped>
.van-tree-select__nav {
  text-align: center;
  background-color: #fff;
  border-right: 1px solid #d9d9d9;
}
.van-sidebar {
  flex: 0.6;
}
.van-sidebar-item {
  background-color: #fff;
}
.van-sidebar-item--select::before {
  height: 0.4rem;
  background: #f26b11;
}
.van-tree-select {
  height: calc(100vh - 0.9rem) !important;
}
.stamp {
  width: 100%;
  height: auto;
  clear: both;
  padding-top: 0.1rem;
  margin-bottom: 0.3rem;
}
.tit,
.title {
  display: flex;
  height: 0.4rem;
  line-height: 0.4rem;
  font-size: 0.14rem;
  height: 0.76rem;
  line-height: 0.76rem;
  padding-left: 0.55rem;
}
.more,
.mored {
  flex: 1;
  text-align: right;
  margin-right: 0.42rem;
}
.shampoo {
  width: 1.5rem;
  float: left;
  text-align: center;
  margin: 0 0.16rem;
}
.shampoo img {
  width: 1.5rem;
}
.shampoo p {
  height: 0.5rem;
  line-height: 0.5rem;
  font-size: 0.22rem;
}
</style>