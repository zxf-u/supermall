<template>
  <div class="tab-control">
    <div class="tab-control-item" :class="{active : curIndex === index}" v-for="(item, index) in titles" :key="item" @click="itemClick(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TabControl',
  props: {
    titles: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      curIndex: 0
    }
  },
  methods: {
    itemClick (index) {
      this.curIndex = index
    }
  }
}
</script>

<style scoped>
.tab-control {
	display: flex;
	height: 40px;
	line-height: 40px;
	text-align: center;
	font-size: 15px;
	background-color: #fff;
}
.tab-control-item {
	flex: 1;
}

.tab-control-item span {
	padding: 5px;
}

.active {
	color: var(--color-high-text);
}

.active span {
	border-bottom: 3px solid var(--color-tint);
}
</style>