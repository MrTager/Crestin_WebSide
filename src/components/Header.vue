<template>
  <div class="header">
    <nav>
       <input type="checkbox" id="check">
       <label v-if="navFlag" class="check_label" for="check">          
       </label>
       <!-- <label class="logo"></label> -->
       <img class="logoImg" src="../assets/images/CRESTIN.png">
       <ul v-if="navFlag">
         <li><a class="active" href="#">主页</a></li>
         <li><a href="#">关于我们</a></li>
         <li><a href="#">产品</a></li>
         <li><a href="#">下载</a></li>
         <li><a href="#">支持</a></li>
       </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      msg: '',
      navFlag:true,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.header{
 // position: relative;
  position: fixed;
  top: 0;
  width: 100%;
  height: 80px;
  z-index: 999;
}
nav{
  background: rgb(31 ,159 ,198);
  height: 80px;
  width: 100%;
}
label.logo{
  // color: white;
  // font-size: 35px;
  // line-height: 80px;
  // padding: 0 100px;
  // font-weight: bold;
  height: 50px;
  width: 150px;
  background-image: url(../assets/images/CRESTIN.png);
  background-repeat: no-repeat;
  background-size: 150px 50px;
  left: 100px;
}
.logoImg{
  width: 178px;
  height: 40px;
  position: absolute;
  left: 180px;
  top: calc(50% - 20px);
}
nav ul{
  float: right;
  margin-right: 20px;
}
nav ul li {
  display: inline-block;
  line-height: 80px;
  margin: 0 5px;
}
nav ul li a{
  color: white;
  font-size: 17px;
  padding: 7px 13px;
  border-radius: 3px;
  text-transform: uppercase;
}
a.active,a:hover{
  background:#1b9bff;
  transition: .5s;
}
.check_label{
  width: 30px;
  height: 30px;
  background-image: url(../assets/images/navBtn.png);
  background-repeat: no-repeat;
  background-size: 30px 30px;
  float:right;
  margin-right: 40px;
  margin-top: 25px;
  cursor: pointer;
  display: none
}
#check{
  display: none;
}
@media (max-width:952px) {
  label.logo{
    font-size: 30px;
    padding-left: 50px;
  }
  .logoImg{
  width: 178px;
  height: 40px;
  position: absolute;
  left: 100px;
  top: calc(50% - 20px);
}
  nav ul li a{
    font-size: 16px;
  }

}
@media (max-width:858px) {
  label.logo{
    font-size: 30px;
    margin-left: auto;
    margin-right: auto;
  }
  .logoImg{
  width: 178px;
  height: 40px;
  position: absolute;
  left: calc(50% - 89px);
  top: calc(50% - 20px);
}
  .check_label{
    display: block;
  }
  ul{
    position: fixed;
    width: 100%;
    height: 100vh;
    background: #2c3e50;
    top: 80px;
    left:-100%;
    text-align: center;
    transition:  all .5s;
  }
  nav ul li {
    display: block;
    margin: 50px 0;
    line-height: 30px;
  }
  nav ul li a {
    font-size: 20px;
  }
  a:hover,a.active{
    background: none;
    color: #0082e6;
  }
  #check:checked ~ ul{
    left:0;
  }
}



</style>