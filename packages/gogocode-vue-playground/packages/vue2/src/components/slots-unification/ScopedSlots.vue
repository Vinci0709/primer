<template>
  <div>
    <slot name="header"></slot>
    <slot></slot>
    <slot name="footer"></slot>
  </div>
</template>
<script>
export default {
  name: 'ScopedSlots',
  mounted() {
    this.$scopedSlots.footer({
      text: "来自子组件的数据",
      name: "aaa",
      id: "aaaaa",
    });
  },
  data() {
    return {
      slots: this.$scopedSlots
    };
  },
};
</script>
