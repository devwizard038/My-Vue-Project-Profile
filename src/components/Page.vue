<script>
import { defineComponent } from "vue"
export default defineComponent({
    name: "Page",
    data(){
        return{
        }
    },
    props: {
        pageId: {
            type: String,
            default: "About"
        }
    },
    methods: {
        print(){
            console.log(this.pageId);
        }
    }
});
</script>
<template>
    <button @click="print">ABC</button>
</template>