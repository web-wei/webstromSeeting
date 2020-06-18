<template>
  <div>
      <common-alert :refNameOuter="refName" class="${name}_page" :title="title" :visible.sync="commonVisible" :appendToBody="true" @close="closeCommonEvent">
        <div class="${name}_wrap">
          asdasdasd
        </div>
      </common-alert>
  </div>  
</template>

<script>
  import CommonAlert from './common/commonAlert'
  import {mapState} from 'vuex'

  export default {
    name: '${name}',
    props: {
      appendToBody: {
        type: Boolean,
        default: false
      },
    },
    components: {
      CommonAlert
    },
    data() {
      return {
        title: '${title}',
        commonVisible: true,
        loading: true,
        refName: '${name}'
      }
    },
    watch: {
      isConnected() {

      },
      commonVisible() {
        // console.log(this.commonVisible);
        if (!this.commonVisible) this.close${closeName}();
      }
    },
    computed: {
      ...mapState([
        'isConnected'
      ])
    },
    methods: {
      close${closeName}() {
        this.commonVisible = false;
      },
      closeCommonEvent() {
        this.$emit('close${closeName}Event', false);
      },
      initData() {
        let that = this;
        this.loading = true;
        this.commonVisible = true;
      },
      clearData() {
        //清除监听事件
        // this.network.removeListeners([3533,3534,3547,3548,3551]);
      }
    },
    mounted() {
      this.initData();
    },
    beforeDestroy() {
      this.clearData();
    }
  }
</script>

<style lang="less">
  .${name}_page {
    .${name}_wrap {
      width: 567px;
      padding: 10px 30px 30px;
    }
  }
</style>