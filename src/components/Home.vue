<template>
    <div class="Home">
        <li  v-on:click='setStoreId()' v-for="(good, index) in list" :key="index" className='pic'>
        <img src='../assets/logo.png' alt=""/>
        <p>{{good.id}}</p>
        </li>
        <div className="clearfix"></div>
    </div>
</template>

<script>
// import '../assets/common.scss'
export default {
  name: 'Home',
  data () {
    return {
      list:[{id:9,name:1,pic:'../assets/logo.png',state:false},{id:8,name:1,pic:'../assets/logo.png',state:false},
            {id:7,name:1,pic:'../assets/logo.png',state:false},{id:6,name:1,pic:'../assets/logo.png',state:false},
            {id:5,name:1,pic:'../assets/logo.png',state:false},{id:4,name:1,pic:'../assets/logo.png',state:false},
            {id:3,name:3,pic:'../assets/logo.png',state:false},{id:2,name:1,pic:'../assets/logo.png',state:false}]
    }
  },
  mounted(){
    this.setStore();
  },
  computed:{

  },
  methods:{
    setStore(){
      this.$store.state.list = this.list;
      var str="<li class='swiper-slide' @click='abc(event)' data-index='0'>"+"</li>";
      // console.log(this.$store.state.list)
    },
    setStoreId(){
      this.$store.state.list[1].id=1;
    }

  }
}
</script>
<style lang="scss" scoped>
  @import '../assets/common.scss';
  @import '../assets/Home.scss'
</style>



