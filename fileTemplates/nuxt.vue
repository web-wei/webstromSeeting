<template>
  <section class="">

  </section>
</template>

<script>
  export default {
    //页面数据
    data() {
        return {}
    },
    /*Nuxt.js 使用了 vue-meta 更新应用的 头部标签(Head) 和 html 属性。
    *使用 head 方法设置当前页面的头部标签。
    *在 head 方法里可通过 this 关键字来获取组件的数据，你可以利用页面组件的数据来设置个性化的 meta 标签。
    */
    head() {
        return {
          //title: this.title,
          //meta: [
          //    { hid: 'description', name: 'description', content: 'My custom description' }
          //]
        }
    },
    /*你可能想要在服务器端获取并渲染数据。Nuxt.js添加了asyncData方法使得你能够在渲染组件之前异步获取数据。
    * asyncData方法会在组件（限于页面组件）每次加载之前被调用。它可以在服务端或路由更新之前被调用。在这个方法被调用的时候，第一个参数被设定为当前页面的上下文对象，你可以利用 asyncData方法来获取数据并返回给当前组件。
    */
    asyncData(context) {
        return {

        }
    },
    /* fetch 方法用于在渲染页面前填充应用的状态树（store）数据， 与 asyncData 方法类似，不同的是它不会设置组件的数据。
        如果页面组件设置了 fetch 方法，它会在组件每次加载前被调用（在服务端或切换至目标路由之前）。
        fetch 方法的第一个参数是页面组件的上下文对象 context，我们可以用 fetch 方法来获取数据填充应用的状态树。为了让获取过程可以异步，你需要返回一个 Promise，Nuxt.js 会等这个 promise 完成后再渲染组件。
    */
    async fetch({store, params}) {
        //let { data } = await axios.get('http://my-api/stars')
        //store.commit('setStars', data)
    },
    /*layouts 根目录下的所有文件都属于个性化布局文件，可以在页面组件中利用 layout 属性来引用。
    *使用 layout 属性来为页面指定使用哪一个布局文件：
    */
    //layout: 'blog',

    /*scrollToTop 属性用于控制页面渲染前是否滚动至页面顶部。
    *默认情况下，从当前页面切换至目标页面时，Nuxt.js 会让目标页面滚动至顶部。但是在嵌套子路由的场景下，Nuxt.js 会保持当前页面的滚动位置，除非在子路由的页面组件中将 scrollToTop 设置为 true。
    */
    // scrollToTop: true,

    /*
    *Nuxt.js 可以让你在动态路由对应的页面组件中配置一个校验方法用于校验动态路由参数的有效性。
    */
    //validate({params, query}) {
      /*
      *return true 如果参数有效
      *return false 参数无效，nuxt停止渲染当前页面并显示错误页面
      *return /^\d+$/.test(params.id) 效验方法不为true，加载404
      */
    //},
    //在实例初始化之后，数据观测 (data observer) 和 event/watcher 事件配置之前被调用。
    beforeCreate() {

    },
    //在实例创建完成后被立即调用。在这一步，实例已完成以下的配置：数据观测 (data observer)，属性和方法的运算，watch/event 事件回调。然而，挂载阶段还没开始， 属性目前不可见。
    created() {

    },
    /*以下生命周期的钩子函数在服务器端渲染期间不被调用*/
    //在挂载开始之前被调用：相关的 render 函数首次被调用
    beforeMount() {

    },
    /*el 被新创建的 vm. 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm. 也在文档内。
    *注意 mounted 不会承诺所有的子组件也都一起被挂载。如果你希望等到整个视图都渲染完毕，可以用 this. 替换掉 mounted：
    */
    mounted() {

    },
    //数据更新时调用，发生在虚拟 DOM 打补丁之前。这里适合在更新之前访问现有的 DOM，比如手动移除已添加的事件监听器。
    beforeUpdate() {

    },
    /*
    *由于数据更改导致的虚拟 DOM 重新渲染和打补丁，在这之后会调用该钩子。
    *当这个钩子被调用时，组件 DOM 已经更新，所以你现在可以执行依赖于 DOM 的操作。然而在大多数情况下，你应该避免在此期间更改状态。如果要相应状态改变，通常最好使用计算属性或 watcher 取而代之。
    *注意 updated 不会承诺所有的子组件也都一起被重绘。如果你希望等到整个视图都重绘完毕，可以用 vm. 替换掉 updated：
    */
    updated() {

    },
    //keep-alive 组件激活时调用。
    activated() {

    },
    //keep-alive 组件停用时调用。
    deactiveted() {

    },
    //实例销毁之前调用。在这一步，实例仍然完全可用。
    beforeDestroy() {

    },
    //Vue 实例销毁后调用。调用后，Vue 实例指示的所有东西都会解绑定，所有的事件监听器会被移除，所有的子实例也会被销毁。
    destroyed() {

    },
    //当捕获一个来自子孙组件的错误时被调用。此钩子会收到三个参数：错误对象、发生错误的组件实例以及一个包含错误来源信息的字符串。此钩子可以返回 false 以阻止该错误继续向上传播。
    errorCaptured(err, vm, info) {

    }
  }
</script>

<style lang="less" scoped>

</style>
