<template>
  <div class="menu__container" @mouseleave="mouseLeave">
    <div class="menu__button">
      <button @click="toggle=!toggle">
        <i class="material-icons left">settings</i>
        <span>ACTIONS</span>
        <i class="material-icons right">arrow_drop_down</i>
      </button>
    </div>
    <div class="menu__items">
      <transition name="fade">
        <ul v-if="toggle">
          <li>Add</li>
          <li>Edit</li>
          <li>Delete</li>
        </ul>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    // toggle: { type: Boolean, default: false }
  },
  data() {
    return {
      toggle: false
    };
  },
  methods: {
    mouseLeave() {
      this.toggle = false;
    }
  }
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.menu__container {
  margin: 5px auto;
  position: relative;
  width: 200px;
}
.menu__button {
  width: 200px;
  box-sizing: border-box;
}
button {
  border: 1px solid #05c591;
  background-color: #05c591;
  padding: 5px;
  font-size: 16px;
  height: 40px;
  width: 200px;
  box-sizing: border-box;
  position: relative;
  border-radius: 2px;
  color: white;
}
.menu__button i {
  display: inline-block;
  margin-top: 5px;
  margin-left: 0;
  position: absolute;
}
.menu__button i.left {
  left: 5px;
  bottom: 7px;
}

.menu__button i.right {
  right: 5px;
  bottom: 7px;
}
.menu__button span {
  display: inline-block;
}
.menu__items {
  position: absolute;
  left: 0;
  top: 40px;
  z-index: 1000;
}
ul {
  list-style-type: none;
  width: 200px;
  box-sizing: border-box;
  margin: 1px auto;
  text-align: center;
  padding-left: 0;
  z-index: 1000;
  border: 1px solid lightgray;
  box-shadow: 1px 1px 7px gray;
}
li {
  padding: 10px;
  background-color: white;
  font-size: 14px;
  border-bottom: 1px solid rgb(241, 240, 240);
  -webkit-transition: max-height 500ms ease;
  -moz-transition: max-height 500ms ease;
  -o-transition: max-height 500ms ease;
  transition: max-height 500ms ease;
}
li:hover {
  background-color: rgb(243, 243, 243);
}
</style>
