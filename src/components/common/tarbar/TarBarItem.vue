<template>
  <div class="tar-bar-item" @click="itemClick">
    <slot v-if="isActive" name="slot-icon"></slot>
    <slot v-else name="slot-icon-active"></slot>
    <div :style="activeStyle">
      <slot name="slot-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TarBarItem',
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  data () {
    return {
    }
  },
  computed: {
    isActive () {
      return this.$route.path.indexOf(this.path) == -1
    },
    activeStyle () {
      return !this.isActive ? { color: this.activeColor } : {}
    }
  },
  methods: {
    itemClick () {
      this.$router.replace(this.path)
    }
  }
}
</script>

<style scoped>
.tar-bar-item {
	flex: 1;
	height: 49px;
	text-align: center;
	font-size: 14px;
}

.tar-bar-item img {
	height: 24px;
	width: 24px;
}
</style>