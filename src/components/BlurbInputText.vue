<template>
  <div class="blurb-input">
    <el-input v-model="input" placeholder="Please input text" maxlength="50" clearable>
      <template slot="append">0/50</template>
      <el-checkbox slot="append" v-model="checked">Translate?</el-checkbox>
    </el-input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      checked: false,
    };
  }
};
</script>

<style>
.blurb-input .el-input__inner {
 border-radius : 4px 0 0 4px;   
}
</style>
