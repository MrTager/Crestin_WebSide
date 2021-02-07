<template>
  <div class="index">
    <Header class="header_h"></Header>
    <Banner class="banner"></Banner>
    <Product></Product>
    <Footer></Footer>
  </div>
</template>

<script>

import Header from '../components/Header'
import Banner from '../components/Banner'
import Footer from '../components/Footer'
import Product from '../components/Product'

export default {
  name: 'Index',
  components:{Header,Banner,Footer,Product},
  data () {
    return {
      pageAllDate:[

        
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header_h{
  
}
.banner{
  margin-top: 80px;
}
</style>
