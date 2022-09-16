<template>
  <TabsContainer>
    <Tab title="Tab 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita delectus modi harum eligendi ad consectetur nam sed natus temporibus itaque.</Tab>
    <Tab title="Tab 2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Est quo autem dolore facere natus. Quo?</Tab>
    <Tab title="Tab 3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt, iure?</Tab>
    <Tab title="Tab 4">Lorem ipsum dolor sit amet.</Tab>
  </TabsContainer>
</template>

<script setup>
  import TabsContainer from './components/TabsContainer.vue';
  import Tab from './components/Tab.vue';
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
