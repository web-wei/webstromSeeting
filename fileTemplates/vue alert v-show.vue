<template>
  <div>
      <common-alert class="${name}_page" :title="title" :refName="'${refName}'" :visible.sync="commonVisible" :appendToBody="true">
        <div class="${name}_wrap">
          asdasdasd
        </div>
      </common-alert>
  </div>  
</template>

<script>
  import CommonAlert from './common/commonAlert'
  import { mapState } from 'vuex'

  export default {
    name: '${name}',
    props: {
      appendToBody: {
        type: Boolean,
        default: false
      },
      visible: {
        type: Boolean,
        default: false
      }
    },
    components: {
      CommonAlert
    },
    data() {
      return {
        title: '${title}',
        commonVisible: false,
        loading: true,
      }
    },
    watch: {
      isConnected() {

      },
      visible() {
        this.commonVisible = this.visible;
        this.visible ? this.initData() : this.clearData();
      },
      commonVisible() {
        this.close(this.commonVisible);
      }
    },
    computed: {
      ...mapState([
        'isConnected'
      ])
    },
    methods: {
      close(val) {
        this.$emit('update:visible', val);
      },
      initData() {
        let that = this;
        this.loading = true;
      },
      clearData() {
        //清除监听事件
        // this.network.removeListeners([3533,3534,3547,3548,3551]);
      }
    },
    mounted() {
      this.commonVisible = this.visible;
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