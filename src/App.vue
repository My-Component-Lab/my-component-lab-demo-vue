<template>
<MConfigProvider :schemas="schemas">
    <h1>My Component Lab Demo</h1>
    <div class="components-container">
        <div class="buttons-container">
            <MButton config-name="primaryButtonOne">Button</MButton>
            <MButton config-name="primaryButtonTwo">Button</MButton>
            <MButton config-name="primaryButtonThree">Button</MButton>
            <MButton config-name="primaryButtonFour">Button</MButton>
        </div>

        <div class="buttons-container">
            <MButton config-name="secondaryButton">Button</MButton>
            <MButton config-name="secondaryButtonTwo">Button</MButton>
            <MButton config-name="secondaryButtonThree">Button</MButton>
            <MButton config-name="secondaryButtonFour">Button</MButton>
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
        MButton
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
    display: flex;
    justify-content: center;
    width: 100%;
    margin-bottom: 20px;
    gap: 20px;
}
</style>