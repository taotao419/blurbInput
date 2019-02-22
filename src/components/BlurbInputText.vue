<template>
  <div class="blurb-input">
    <!--the blurb Id should be displayed in html comment-->
    <input type="hidden" :value="blurbId">
    <el-input v-model="input" clearable>
      <template slot="append" >
        <span v-show="!hasMaxLength"
          :class="{'normal':lessMaxLength,'alarm':!lessMaxLength}"
        >{{input.length}} / {{maxlength}} &nbsp;</span>
      </template>
      <el-checkbox slot="append" v-model="translated">Translate?</el-checkbox>
    </el-input>
  </div>
</template>

<script>
//read prop maxlength
//show xx/50 ,if xx>50 then display red but not block user
//typing word
export default {
  props: {
    value: Object,
    maxlength: Number
  },
  data() {
    return {
      input: this.value.input, //obj.input,
      blurbId: this.value.blurbId,
      translated: this.value.translated
    };
  },
  computed: {
    lessMaxLength: function() {
      return this.input.length < this.maxlength;
    },
    hasMaxLength: function() {
      return this.maxlength === undefined;
    }
  }
};
</script>

<style>
.blurb-input .el-input__inner {
  border-radius: 4px 0 0 4px;
}

.blurb-input .alarm {
  font-weight: bold;
  color: red;
}

.blurb-input .normal {
  color: green;
}
</style>
