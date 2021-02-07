<template>
  <div class="banner">
    <img class="bannerImg" src="../assets/images/banner.png">
  </div>
</template>
<script>
export default {
  name: 'Banner',
  data () {
    return {
      msg: '',
      url:'',
    }
  },
}
</script>
<style lang="scss" scoped>
.banner{
    width: 100%;
    max-height: 650px;
}
.bannerImg{
    width: 100%;
    max-height: 650px;
}
</style>
