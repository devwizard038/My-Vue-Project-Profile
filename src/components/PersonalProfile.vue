<script>
import { defineComponent } from "vue";
export default defineComponent({
  name: "PersonalProfile",
  data() {
    return{
      isActive: false
    }
  },
  props: {
    username: {
      type: String,
      required: true
    },
    aptitude: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    phone: {
      type: String,
      required: true
    },
    birthday: {
      type: String,
      required: true
    },
    location: {
      type: String,
      required: true
    }
  },
  methods: {
    showContent(){
      this.isActive = !this.isActive
    }
  }
});
</script>

<template>
  <aside class="sidebar" :class = "{active: isActive}">

    <div class="sidebar-info">

      <figure class="avatar-box">
        <img src="../assets/images/my-avatar.jpg" alt="Albert Hikashi" width="80" style="border-radius: 100%;">
      </figure>

      <div class="info-content">
        <h1 class="name" title="Albert Hikashi">{{ name }}</h1>

        <p class="title">{{ aptitude }}</p>
      </div>

      <button class="info_more-btn" @click="showContent">
        <span>Show Contacts</span>

        <ion-icon name="chevron-down"></ion-icon>
      </button>

    </div>

    <div class="sidebar-info_more">

      <div class="separator"></div>

      <ul class="contacts-list">

        <li class="contact-item">

          <div class="icon-box">
            <ion-icon name="mail-outline"></ion-icon>
          </div>

          <div class="contact-info">
            <p class="contact-title">Email</p>

            <a href="mailto:richard@example.com" class="contact-link">{{ email }}</a>
          </div>

        </li>

        <li class="contact-item">

          <div class="icon-box">
            <ion-icon name="phone-portrait-outline"></ion-icon>
          </div>

          <div class="contact-info">
            <p class="contact-title">Phone</p>

            <a href="tel:+12133522795" class="contact-link"> {{ phone }} </a>
          </div>

        </li>

        <li class="contact-item">

          <div class="icon-box">
            <ion-icon name="calendar-outline"></ion-icon>
          </div>

          <div class="contact-info">
            <p class="contact-title">Birthday</p>

            <time datetime="1982-06-23">{{ birthday }}</time>
          </div>

        </li>

        <li class="contact-item">

          <div class="icon-box">
            <ion-icon name="location-outline"></ion-icon>
          </div>

          <div class="contact-info">
            <p class="contact-title">Location</p>

            <address>{{ location }}</address>
          </div>

        </li>

      </ul>

    </div>
  </aside>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
