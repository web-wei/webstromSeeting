<template>
  <div>
    <section :ref="'${refName}'" class="commonAlert_page ${name}_page"
             :style="{ position: appendToBody ? 'fixed' : 'absolute', background: appendToBody ? 'rgba(0,0,0,0.4)' : 'rgba(0,0,0,0.8)' }"
             @click.self="close">
      <div class="commonAlert_wrap ${name}_wrap">
        <span class="commonAlert_close iconfont ${name}_close" @click="close">&#xe613;</span>
        <h2 class="commonAlert_title ${name}_title">{{title}}</h2>
        <div class="commonAlert_main ${name}_main">

        </div>
      </div>
    </section>
  </div>
</template>

<script>
  import {commonAlert} from './mixin'

  export default {
    name: '${name}',
    mixins: [commonAlert],
    props: {
      appendToBody: {
        type: Boolean,
        default: false
      },
    },
    components: {

    },
    data() {
      return {
        title: '${title}',
        commonVisible: true,
        loading: true,
      }
    },
    watch: {
      isConnected() {

      }
    },
    computed: {

    },
    methods: {
      close() {
        this.$emit('close${closeName}Event', false);
      },
      initData() {
        let that = this;
        this.loading = true;
        this.afterOpen();
      },
      clearData() {
        this.beforeClose();
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