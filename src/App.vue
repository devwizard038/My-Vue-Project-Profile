<script setup>
import PersonalProfile from './components/PersonalProfile.vue'
import Personal_main from './components/Personal_main.vue'

</script>

<template>
  <main>
    <PersonalProfile username = "Albert Hikashi"
                    aptitude = "Web developer" 
                    email = "wizard38.software@gmail.com" 
                    phone = "+1 808-573-7352"
                    birthday = "Mar 8 1997"
                    location = "Makawao, Hawaii, USA"/>
    <Personal_main />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
