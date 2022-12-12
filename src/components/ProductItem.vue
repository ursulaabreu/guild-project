<template>
  <div>
    {{ item.type }}
  </div>
  <div>
    {{ item.name }}
  </div>
  <div>
    {{ item.description }}
  </div>
  <div>
    {{ item.stock }}
  </div>
</template>

<script>
export default {
  name: 'ProductItem',
  // Special keyword which stands for properties. It can be registered on a component to pass data from a parent component to one of its children components.
  props: {
    item: null,
  },
};
</script>

<style scoped></style>
