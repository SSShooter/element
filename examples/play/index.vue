<template>
  <div style="margin: 20px;">
    <el-button @click="readonly = !readonly">toggle</el-button>
    <el-input :readonly="readonly" v-model="input" placeholder="请输入内容"></el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      readonly: true
    };
  },
  methods: {
    handleChange(val, oval) {
      console.log(val, oval);
    }
  }
};
</script>
