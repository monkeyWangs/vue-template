<template>
  <div class="layout">
    <% _.forEach(data.components, function(component){ %>
      <<%- component.name %> :data="component.data"></<%- component.name %>>
    <% }) %>
  </div>
</template>

<script>
  <% _.forEach(data.components, function(component){ %>
    import t{{component.name}} from 'components/{{component.source}}.vue'
  <% }) %>
export default {
  name: 'app',
  components: {
  <% _.forEach(data.components, function(component){ %>
    {{component.name}},
  <% }) %>
  }
}
</script>

<style lang="scss">
  .header {
    width: 100%;
    height: 50px;
    border: 1px solid blue;
  }
  .footer {
    width: 100%;
    height: 50px;
    border: 1px solid red;
  }
  .container {
    width: 100%;
    height: 500px;
    border: 1px solid black;
  }
</style>
