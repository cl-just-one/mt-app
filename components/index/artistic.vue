<template>
  <section class="m-istyle">
    <dl>
      <dt>有格调</dt>
      <dd
        kind="all"
        keyword="景点">全部</dd>
      <dd
        kind="part"
        keyword="美食">约会聚餐</dd>
      <dd
        kind="spa"
        keyword="丽人">丽人SPA</dd>
      <dd
        kind="travel"
        keyword="旅游">电影演出</dd>
      <dd
        kind="all"
        keyword="">品质出游</dd>
    </dl>
    <ul class="ibody">
      <li
        v-for="item in cur"
        :key="item.title">
        <el-card
          :body-style="{ padding: '0px' }"
          shadow="never">
          <img
            src="a"
            class="image">
          <ul class="cbody">
            <li class="title">1</li>
            <li class="pos">6</li>
            <li class="price">7</li>
          </ul>
        </el-card>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data: () => {
    return {
      kind: "all",
      list: {
        all: [],
        part: [],
        spa: [],
        movie: [],
        travel: []
      }
    }
  },
  computed: {
    cur: function () {
      return this.list[this.kind]
    }
  },
  async mounted () {
    let self = this
    // let {status, data: {count, pois}} = await self.$axios.get('/search/resultsBykeyword', {
    //   params: {
    //     keyword: '景点',
    //     city: self.$store.state.geo.position.city
    //     city: '北京'
    //   }
    // })
  }
}
</script>

<style lang="scss">
  @import '@/assets/css/index/artistic.scss'
</style>
