<template>
  <div class="home">
    <div>
      <router-link to="/mockdatatest">MockDataTest</router-link> |
      <router-link to="/charttest">chartTest</router-link> |
      <router-link to="/dynamictabletest">dynamicTableTest</router-link> |
      <router-link to="/polylinetest">polylineTest</router-link> |
      <router-link to="/bmaptest">bmapTest</router-link> |
      <router-link to="/bmapgltest">bmapGLTest</router-link> |
      <router-link to="/amaplocatest">amapLocaTest</router-link> |
      <router-link to="/videocapturetest">videoCaptureTest</router-link> |
      <router-link to="/echartMapTest">echart地图显示测试</router-link> |
      <router-link to="/somethingTest">杂七杂八测试</router-link> |
      <router-link to="/bigscreen">响应式大屏</router-link> |
    </div>
    <div>
      <el-button type="primary" @click="show1">百度地图选坐标组件测试</el-button>
    </div>
    <router-view />
    <point-select-dialog ref="pointSelectDialog" @confirmCllick="bMapPointSelect" />
  </div>
</template>

<script>
export default {
  name: 'Home',
  components: {
    PointSelectDialog: () => import ('@/components/bmap/pointSelect.vue')
  },
  methods: {
    show1() {
      this.$refs.pointSelectDialog.show()
    },
    bMapPointSelect(res) {
      console.log(res)
    }
  }
}
</script>
