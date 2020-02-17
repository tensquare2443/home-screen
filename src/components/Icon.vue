<template>
  <div class="app">
    <img
      :src="require(`../assets/icons/${file}`)"
      alt=""
      class="app__icon"
      :class="{
        selecting: selectedIcon,
        selected: selectedIcon.name === name
      }"
    />
    <div class="app__label">
      <p class="app__label-txt">{{ name }}</p>
    </div>
  </div>
</template>

<script>
// "-webkit-user-select: none" on ".app" is messing up firefox
export default {
  props: ["name", "file", "selectedIcon"]
};
</script>
