<template>
<div>
    <h2>Parent Component</h2>
    <ChildComponent :message="parentMessage" :parentname="parentName" />
</div>
</template>

  
<script>
import ChildComponent from './ChildComponent.vue';

export default {
    components: {
        ChildComponent
    },
    data() {
        return {
            parentMessage: 'Hello from Parent!',
            parentName: 'John Doe'
        };
    }
};
</script>
