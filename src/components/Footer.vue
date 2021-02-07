<template>
  <div class="footer">
        <div class="contact_txt">Contact Us</div>
        <div class="contact_info">
            <p><span class="span_1"></span>  Cell:0086-18042026794</p>
            <p><span class="span_2"></span>  E-mail:crestinsmart@gmail.com</p>
            <p><span class="span_3"></span>  Add:1713 Ironwood Lane Milpitas, CA95035</p>
        </div>
  </div>
</template>
<script>
export default {
  name: 'Footer',
  data () {
    return {
      msg: '',
    }
  }
}
</script>
<style lang="scss" scoped>
.footer{
    width: 100%;
    height: 200px;
    background-color: rgb(31,159,198);
    position: relative;
}
.contact_txt{
    width: 600px;
    height: 100px;
    font-size: 54px;
    color: white;
    text-align: center;
    line-height: 100px;
    position: absolute;
    left: calc(50% - 600px);
    top: calc(50% - 50px);
}
.contact_info{
    width: 600px;
    height: 100px;
    font-size: 20px;
    color: white;
    text-align: left;
    position: absolute;
    left: 50%;
    top: calc(50% - 50px);
    line-height: 30px;
    span{
        width: 20px;
        height: 20px;
    }
}
.span_1{
    background-image: url(../assets/images/span_call.png);
    background-repeat: no-repeat;
    background-size: 20px 20px;
    display: inline-block;
}
.span_2{
    background-image: url(../assets/images/span_email.png);
    background-repeat: no-repeat;
    background-size: 20px 20px;
    display: inline-block;
}
.span_3{
    background-image: url(../assets/images/span_address.png);
    background-repeat: no-repeat;
    background-size: 20px 20px;
    display: inline-block;
}
</style>
