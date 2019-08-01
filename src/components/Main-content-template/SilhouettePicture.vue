<template>
  <div>
    <Row type="flex" justify="center">
      <Col span="16">
      <div class="Pictures-titlebar">
        <div>
          <Icon type="ios-film-outline" size="20" class="icon" color="#2d8cf0" />
          <span class="name">水库掠影</span>
        </div>
        <div>
          <a href="#">更多>></a>
        </div>
        </div>
      </Col>
      <Col span="16">
        <div class="Pictures">
          <div></div>
          <div class="imgs" v-for="item in Picturess" :key="item.id">
            <img :src="item.img" alt />
            <div class="site-name">{{item.names}}</div>
          </div>
        </div>
      </Col>
    </Row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Picturess: [
        {
          img: require("../../assets/9.jpg"),
          names: "光山水库"
        },
        {
          img: require("../../assets/10.jpg"),
          names: "半山水库"
        },
        {
          img: require("../../assets/11.jpg"),
          names: "将军山水库"
        },
        {
          img: require("../../assets/12.jpg"),
          names: "洪水沟水库"
        }
      ]
    };
  }
};
</script>

<style>
.Pictures-titlebar{
    display: flex;
    justify-content: space-between;
    padding: 10px 12px;
}
.Pictures-titlebar .name{
    font-size: 18px;
    color:#333;
    font-weight: bold
}
.Pictures-titlebar a{
    color:#ccc
}
.Pictures-titlebar .icon{
    display: inline-block;
    vertical-align: top;
    margin-right: 5px;
}
.Pictures {
  display: flex;
  justify-content: space-between;
}
.Pictures .imgs {
  width: 245px;
  height: 150px;
  position: relative;
}
.Pictures .imgs img {
  display: block;
  width: 100%;
  height: 100%;
}
.Pictures .site-name {
  position: absolute;
  top: 10px;
  left: 10px;
  padding: 2px 10px;
  background: #2d8cf0;
  font-size: 14px;
  color: #fff;
}
</style>
