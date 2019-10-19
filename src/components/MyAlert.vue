<template>
<Modal
  v-model="modelStatus"
  @on-visible-change="modalChange"
>
</Modal>
</template>

<script>
/* eslint-disable */
export default {
  props: {
    isAlertOn: {
      type: Boolean,
      default: false
    }
  },

  watch: {
    isAlertOn(status) {
      this.modelStatus = status;
    }
  },

  data() {
    return {
      modelStatus: false
    }
  },

  methods: {
    modalChange(curStatus) {
      console.log(this.modelStatus, curStatus);
      this.$emit('modalStatusChange', curStatus);
    }
  }
}
</script>