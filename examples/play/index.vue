<template>
  <div style="margin: 20px;">
    <el-input v-model="input" placeholder="请输入内容"></el-input>
    <el-cascader
      v-model="input"
      :options="[{ value: 111 }, { value: 1222 }]"
      @change="handleChange"
    ></el-cascader>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "Hello Element UI!"
    };
  },
  methods: {
    handleChange(val, oval) {
      console.log(val, oval);
    }
  }
};
</script>
