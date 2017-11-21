<template>
  <div>
    <ul>
      <li v-for="item in shoppingList">
        {{item}}
      </li>
    </ul>
  </div>
</template>

<script>
import EventBus from '../EventBus';
export default {
  props: ['shoppingList'],
  created() {
    EventBus.$on('addShoppingItem', (item) => {
      console.log(`There was an item added! ${item}`);
    })
  }
}
</script>

<style>

</style>
