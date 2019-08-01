<template>
  <div>
    <div class="policies">
      <div class="policies-titlebar">
        <div>
          <Icon type="md-list-box" color="#2d8cf0" size="20" class="icon" />
          <span class="policies-title">政策法规</span>
        </div>
        <div>
          <a href="#">更多>></a>
        </div>
      </div>
      <div class="content">
        <div class="inner" v-for="item in policies" :key="item.id">
          <div>
            <em></em>
          </div>
          <div>{{item.title}}</div>
        </div>
       
      
      </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            policies:[
                {
                    title:'两站进行时系列报道二:淮安"两违"整治新突破,江湖保'
                },
                 {
                    title:'两站进行时系列报道二:江湖保卫战正酣'
                },
                 {
                    title:'两站进行时系列报道二:江湖保卫战正酣'
                },
                 {
                    title:'两站进行时系列报道二:江湖保卫战正酣'
                },
                 {
                    title:'两站进行时系列报道二:淮安"两违"整治新突破,江湖保'
                },
                 {
                    title:'两站进行时系列报道二:江湖保卫战正酣'
                },
                 {
                    title:'两站进行时系列报道二:江湖保卫战正酣'
                },
            ]
        }
    }
};
</script>

<style>
.policies {
  margin-left: 10px;
}
.policies .policies-titlebar {
  display: flex;
  justify-content: space-between;
  padding: 10px ;
}
.policies .policies-titlebar .policies-title {
  font-size: 18px;
  color: #333;
  font-weight: bold;
 
}
.policies .policies-titlebar .icon {
  display: inline-block;
  vertical-align: top;
  margin-right: 5px;
}
.policies .policies-titlebar a {
  color: #ccc;
}
.policies .content {
  background: #fff;
  padding: 10px;
}

.policies .content .inner {
  display: flex;
  margin-bottom:10px;
  padding:16px 0
}

.policies .content .inner :hover{
    color:#2d8cf0;
    cursor: pointer;
}

.policies .content .inner em{
    width:5px;
    height:5px;
    display: inline-block;
    background: #333;
    border-radius: 50%;
    margin:0 10px 
}
</style>
