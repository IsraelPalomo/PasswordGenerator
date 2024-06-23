<template>
  <div class="button" @click="$emit('btnAction')" >
    Generate Password
  </div>
</template>

<script setup>



</script>

<style lang="css" scoped>
 .button {
    width: fit-content;
    padding: .5rem 2rem;
    border-radius: 8px;
    background-color: rgb(71, 31, 190);
    color: #ffffff;
    display: flex;
    align-items: center;
    align-items: center;
    cursor: pointer;
  }
  .button:hover {
    background-color: rgb(62, 28, 165);
  }
</style>