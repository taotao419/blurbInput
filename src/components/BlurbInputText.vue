<template>
  <div class="blurb-input">
    <el-input v-model="input" placeholder="Please input text" clearable>
      <template slot="append">
        <span
          :class="{'normal':lessMaxLength,'alarm':!lessMaxLength}"
        >{{input.length}} / {{maxlength}}</span>
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
     obj: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      input: obj.input,
      translated: obj.translated
    };
  },
  computed: {
    lessMaxLength: function() {
      return this.input.length < this.maxlength;
    }
  }
};
</script>

<style>
.blurb-input .el-input__inner {
  border-radius: 4px 0 0 4px;
}

.alarm {
  font-weight: bold;
  color: red;
}

.normal {
  color: green;
}
</style>
