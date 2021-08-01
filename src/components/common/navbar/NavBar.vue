<template>
  <div class="nav-bar">
    <div class="left">
      <slot name="left"></slot>
    </div>
    <div class="center">
      <slot name="center"></slot>
    </div>
    <div class="right">
      <slot name="right"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style scoped>
.nav-bar {
	display: flex;
	height: 44px;
	box-shadow: 0 1px 1px rgba(100, 100, 100, .1);
	background-color: var(--color-tint);
	color: #fff;
}
.left {
	width: 60px;
	/* background-color: rebeccapurple; */
}
.center {
	flex: 1;
	/* background-color: royalblue; */
	display: flex;
	justify-content: center;
	align-items: center;
}
.right {
	width: 60px;
	/* background-color: rebeccapurple; */
}
</style>
