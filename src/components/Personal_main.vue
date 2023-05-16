<script>
import { defineComponent } from "vue"

export default defineComponent({
  name: "Personal_main",
  data(){
    return{
      pageId: "About"
    }
  },
  props: {},
  methods: {}
});
</script>

<script setup>
import Navbar from './Navbar.vue'
import Page from './Page.vue'
</script>

<template>
  <div class="main-content">
    <Navbar @response="(_pageId) => pageId = _pageId"/>
    <Page :page-id = "pageId"/>
  </div>
</template>
