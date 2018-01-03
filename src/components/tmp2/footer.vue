<template>
  <div class="footer">
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
