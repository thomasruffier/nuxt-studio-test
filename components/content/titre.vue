<template>
  <component :is="as" :class="classComputed">
    <txt><slot /></txt>
  </component>
</template>

<script setup>
const props = defineProps({
  as: { default: "div", type: String },
  class: { default: "", type: String },
  type: { default: "1", type: String },
});
const classComputed = computed(() => {
  let temp = [];
  if (props.type == "1") {
    temp =
      "font-Titre sm:text-[3.8125rem] text-white font-bold sm:leading-[4rem] text-[2.5rem] leading-10";
  }
  if (props.type == "2") {
    temp =
      "font-Titre sm:text-[2.5rem] text-[1.8rem] text-white font-bold leading-10";
  }
  if (props.type == "3") {
    temp = "font-Titre text-[2.5rem] text-white font-bold text-center";
  }
  if (props.type == "4") {
    temp =
      "text-[1.2rem] text-white  text-center font-Titre font-light uppercase";
  }
  return [temp, props.class];
});
</script>
