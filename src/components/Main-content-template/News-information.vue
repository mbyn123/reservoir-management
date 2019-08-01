<template>
  <div>
    <Row type="flex" justify="center">
      <Col span="16">
        <Row>
          <Col span="17">
            <div class="news">
              <div class="news-titlebar">
                <div>
                  <Icon type="md-paper" color="#2d8cf0" size="20" class="icon" />
                  <span class="name">新闻资讯</span>
                </div>
                <div>
                  <a href="#">更多>></a>
                </div>
              </div>
              <div class="content">
                  <div class="news-item" v-for="item in news" :key="item.id">
                      <div class="img"><img :src=item.img alt=""></div>
                      <div class="inner">
                          <div class="news-title">{{item.title}}</div>
                          <div class="news-time">{{item.time}}</div>
                          <div class="news-content">{{item.content}}</div>
                      </div>
                  </div>
                  
              </div>
            </div>
          </Col>
          <Col span="7">
           <policies/>
          </Col>
        </Row>
      </Col>
    </Row>
  </div>
</template>

<script>
import Policies from "./Policies"
export default {
    data(){
        return{
            news:[
                {
                    img:require("../../assets/6.jpg"),
                    title:"只依赖于注意力机制,不包含任何循环神经网络",
                    time:"2019-07-16",
                    content:"只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络....",
                },
                  {
                    img:require("../../assets/6.jpg"),
                    title:"只依赖于注意力机制,不包含任何循环神经网络",
                    time:"2019-07-16",
                    content:"只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络....",
                },
                  {
                    img:require("../../assets/6.jpg"),
                    title:"只依赖于注意力机制,不包含任何循环神经网络",
                    time:"2019-07-16",
                    content:"只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络,只依赖于注意力机制,不包含任何循环神经网络....",
                },
            ]
        }
    },
    components:{
      Policies
    }
};
</script>

<style>

.news .news-titlebar {
  display: flex;
  justify-content: space-between;
  padding: 10px
}

.news .news-titlebar .name {
  font-size: 18px;
  color: #333;
  font-weight: bold;
}

.news .news-titlebar .icon {
  display: inline-block;
  vertical-align:top;
  margin-right: 5px;
}

.news .news-titlebar a{
    color:#ccc
}


.news .content .news-item{
    display: flex;
    background: #fff;
    margin-bottom: 10px;
    
}

.news .content .news-item:hover{
    box-shadow: -1px 0px 8px -2px rgba(77, 73, 77, 1);
    }

.news .content .news-item .img{
    width:300px;
    height:150px;
    padding: 10px;
}
.news .content .news-item .img img{
    display: block;
    width:100%;
    height:100%;
}
.news .content .news-item .inner{
   padding-right: 10px;
}
.news-item .inner .news-title{
    font-size: 16px;
    color:#333;
    font-weight: bold;
    padding: 10px 0 5px 0;
    cursor: pointer;
}

.news-item .inner .news-title:hover{
    color:#2d8cf0
}
.news-item .inner .news-time{
    color:#333;
    padding: 5px 0 5px 0;
}
.news-item .inner .news-content{
    padding: 20px 0
}
</style>
