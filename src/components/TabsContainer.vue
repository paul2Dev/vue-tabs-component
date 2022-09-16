<template>
    <div class="tabs">
        <ul class="tabs__header">
            <li 
                v-for="title in tabTitles" 
                :key="title"
                :class="{ selected: title == selectedTitle }"
                @click="selectedTitle = title"
            >
                {{ title }}
            </li>
        </ul>
        <slot />
    </div>
</template>

<script>
import { ref, provide } from 'vue'
export default {
    setup(props, { slots }) {
        
        const tabTitles = ref(slots.default().map((tab) => tab.props.title))
        const selectedTitle = ref(tabTitles.value[0])

        provide('selectedTitle', selectedTitle)

        return {
            tabTitles,
            selectedTitle
        }

    }
}
</script>

<style scoped>
.tabs {
    max-width: 500px;
    margin: 0 auto;
}
.tabs__header {
    margin-bottom: 10px;
    list-style: none;
    padding: 0;
    display: flex;

}

.tabs__header li{
    width: 100px;
    text-align: center;
    padding: 15px;
    margin-right: 15px;
    background-color: #41B883;
    border-radius: 5px;
    color: white;
    cursor: pointer;
    transition: 0.2s all ease-in;
}

.tabs__header li.selected{
    background-color: #34495E;
}
</style>