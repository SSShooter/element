<template>
  <div style="margin: 20px;">
    <el-input readonly v-model="input" placeholder="请输入内容"></el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: ""
    };
  },
  methods: {
    handleChange(val, oval) {
      console.log(val, oval);
    }
  }
};
</script>
