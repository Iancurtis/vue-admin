<template>
  <div>
    <input type="number" id="name" v-model.number="msg">
    <label for="name">{{msg}}</label>
    <mycomponent
      :foo='a'
      :bar='msg'
    >
    </mycomponent>

    <div class='show-test'>
    <button v-on:click='show = !show'>toggle</button>
    <!--<transition name='fade'>-->
    <transition mode="out-in"
        enter-active-class="fadeIn"
        leave-active-class="fadeOut"
        appear>
      <p class='animated' v-show="show">I'm showing now</p>
    </transition>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import mycomponent from './my-component'
export default {
  data () {
    return {
      show: false,
      msg: '',
      a: 'T',
      b: 'F'
    }
  },
  components: {
    mycomponent
  }
}
</script>

<style lang="scss" scoped>
select {
  background-color: red;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s
}
.fade-enter, .fade-leave-active {
  opacity: 0
}
</style>
