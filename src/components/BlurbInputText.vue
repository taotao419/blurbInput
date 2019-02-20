<template>
  <div class="blurb-input">
    <div style="float:left">
      <el-input v-model="input" placeholder="Please input text"></el-input>
    </div>
    <div style="float:left">
        <el-checkbox-button v-model="checked"><i class="fa fa-language" aria-hidden="true"></i></el-checkbox-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      checked: true,
    };
  }
};
</script>

<style>
.blurb-input .el-input__inner {
 border-radius : 4px 0 0 4px;   
}
</style>
