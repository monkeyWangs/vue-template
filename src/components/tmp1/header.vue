<template>
  <div class="header">
    {{data.msg}}
  </div>
</template>
<script>
  export default{
    props: {
      data: {
        type: Object,
        default: {}
      }
    }
  }
</script>
