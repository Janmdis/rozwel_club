<template>
  <ul>
    <li class="item" :class="activate === 'all'?'activate':''" @click="setCategory()">全部内容</li>
    <li v-for="(c,index) in category" :key="c.key" class="item" :class="index === activate ? 'activate' : ''" @click="setCategory(c._id,index)">
      <span>{{c._id | typeFormat}}</span>
      <type>{{c.count}}</type>
    </li>
  </ul>
</template>

<script>
import Type from '@/components/base/type/type';
import { typeFormat } from '@/common/js/common';
export default {
  data() {
    return {
      activate: 'all'
    }
  },
  props: {
    category: {
      type: Array,
      default: ()=>[]
    }
  },
  components: {
    Type
  },
  filters: {
    typeFormat
  },
  methods: {
    setCategory(cid = -1, index = -1) {
      if(index !== -1){
        this.activate = index;
      }else {
        this.setAllC();
      }
      this.$emit('setCategory',cid);
    },
    setAllC() {
      this.activate = 'all';
    }
  }
};
</script>

<style lang="scss" scoped>
.item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: space-between;
  cursor: pointer;
  border-left: 2px solid #ddd;
  &.activate {
    border-left: 2px solid blue;
  }
}
</style>
