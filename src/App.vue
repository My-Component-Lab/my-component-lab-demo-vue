<template>
<MConfigProvider :schemas="schemas">
    <h1>My Component Lab Demo</h1>
    <div class="components-container">
        <div class="buttons-container">
            <MButton config-name="primaryBtnSmall">Button Text</MButton>
            <MButton config-name="primaryBtnMedium">Button Text</MButton>
            <MButton config-name="primaryBtnLarge">Button Text</MButton>
            <MButton config-name="primaryBtnXL">Button Text</MButton>
            <MButton config-name="primaryBtnXXL">Button Text</MButton>
        </div>
    </div>
</MConfigProvider>
</template>


<script lang="ts">
import { defineComponent } from 'vue';
import { MConfigProvider, MButton } from "my-component-lab";
import schemas from "../my-component-schema.config.json";
export default defineComponent({
    components: {
        MConfigProvider,
        MButton,
    },
    setup() {
        return {
            schemas
        }
    }
})
</script>

<style scoped>
h1 {
    font-size: 3rem;
    color: #FFF;
    text-align: center;
    margin-bottom: 3rem;
    margin-top: 5rem;
}
.components-container {
    max-width: 1200px;
    margin: auto;
}
.buttons-container {
    align-items: flex-start;
    display: flex;
    justify-content: center;
    width: 100%;
    margin-bottom: 20px;
    gap: 20px;
}

button {
    display: block;
}
</style>