<template>
  <div style="margin: 20px;">
    <el-button @click="readonly = !readonly">toggle</el-button>
    <el-input :readonly="readonly" type="textarea" v-model="input" placeholder="请输入内容"></el-input>
    <el-select :readonly="readonly" v-model="value" @change="handleChange" placeholder="请选择">
      <el-option v-for="item in options" :key="item.value" :label="item.label" :value="item.value"></el-option>
    </el-select>
    <el-date-picker :readonly="readonly" v-model="value1" type="date" placeholder="选择日期"></el-date-picker>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      value1: "",
      readonly: true,
      options: [
        {
          value: "选项1",
          label: "黄金糕"
        },
        {
          value: "选项2",
          label: "双皮奶"
        },
        {
          value: "选项3",
          label: "蚵仔煎"
        },
        {
          value: "选项4",
          label: "龙须面"
        },
        {
          value: "选项5",
          label: "北京烤鸭"
        }
      ],
      value: ""
    };
  },
  methods: {
    handleChange(val, oval) {
      console.log(val, oval);
    }
  }
};
</script>
