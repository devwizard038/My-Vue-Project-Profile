<script>
import { defineComponent } from "vue"
export default defineComponent({
    name: "Page",
    data(){
        return{
            testimonialName: "",
            testimonialText: "",
            isModal: false
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
        },
        onTestimonial(e){
            this.testimonialName = e.currentTarget.children[0].innerHTML
            this.testimonialText = e.currentTarget.children[1].children[0].innerHTML
            this.isModal = true;
        },
        onModalCancel(e){
            console.log(e.target, e.currentTarget);
            if(e.target == e.currentTarget)
                this.isModal = false;
        }
    }
});
</script>
<template>
    <article class="about" :class="{active: pageId == 'About'}" data-page="about">

        <header>
        <h2 class="h2 article-title">About me</h2>
        </header>

        <section class="about-text">
        <p>
            I'm a creative developer from Hawaii, USA. As a full stack and mobile developer, I have the unique ability to design and develop software that's optimized for both desktop and mobile platforms. With my comprehensive knowledge of both front-end and back-end development, I can ensure that your application is optimized for performance, security, and scalability. Whether it's building web applications, developing mobile apps, or creating e-commerce platforms, I have the technical skills and experience necessary to deliver robust solutions that meet the needs of your business. 
        </p>

        <p>
            From strategy and design to implementation and testing, I have been involved in every stage of the development process and I am committed to delivering solutions that exceed expectations.
        </p>
        </section>


        <!--
        - service
        -->

        <section class="service">

        <h3 class="h3 service-title">What i'm doing</h3>

        <ul class="service-list">

            <li class="service-item">

            <div class="service-icon-box">
                <img src="../assets/images/icon-design.svg
                " alt="design icon" width="40">
            </div>

            <div class="service-content-box">
                <h4 class="h4 service-item-title">Web design</h4>

                <p class="service-item-text">
                The most modern and high-quality design made at a professional level.
                </p>
            </div>

            </li>

            <li class="service-item">

            <div class="service-icon-box">
                <img src="../assets/images/icon-dev.svg" alt="Web development icon" width="40">
            </div>

            <div class="service-content-box">
                <h4 class="h4 service-item-title">Web development</h4>

                <p class="service-item-text">
                High-quality development of sites at the professional level.
                </p>
            </div>

            </li>

            <li class="service-item">

            <div class="service-icon-box">
                <img src="../assets/images/icon-app.svg" alt="mobile app icon" width="40">
            </div>

            <div class="service-content-box">
                <h4 class="h4 service-item-title">Mobile apps</h4>

                <p class="service-item-text">
                Professional development of applications for iOS and Android.
                </p>
            </div>

            </li>

        </ul>

        </section>


        <!--
        - testimonials
        -->

        <section class="testimonials">

        <h3 class="h3 testimonials-title">Testimonials</h3>

        <ul class="testimonials-list has-scrollbar">

            <li class="testimonials-item">
            <div class="content-card" @click="onTestimonial">

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Edward Johnson</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav was hired to create a remote control system for me. He showed himself as a gifted developer and did his best to satisfy my demands. He is a talented backend developer and creative front-end designer. He is very friendly and cool, a client-friendly developer. I look forward to working with him further.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" @click="onTestimonial">

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Chris Anderson</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav showed a good skill of project management and maintenance. He is a database expert and he is really good at debugging. He solved our site's problem perfectly. Looking forward to working with him again.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" @click="onTestimonial">

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Venkat Muhammad</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav worked on a small project using google search api. He showed himself as a good view of programming and introduced me to the world of apis. He is a good developer and really client-friendly. Looking forward to working with him again.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" @click="onTestimonial">

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Sonia Moka</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav is a PHP and C master! He worked on a project of converting C project to PHP and he showed his skills of logistics. He is a cryptography expert, too. Looking forward to working with him again.
                </p>
                </div>

            </div>
            </li>

        </ul>

        </section>


        <!--
        - testimonials modal
        -->

        <div class="modal-container" :class="{ active: isModal }" @click="onModalCancel">

        <div class="overlay"></div>

        <section class="testimonials-modal">

            <button class="modal-close-btn" @click="onModalCancel">
            <ion-icon name="close-outline" @click="onModalCancel"></ion-icon>
            </button>

            <div class="modal-content">

            <h4 class="h3 modal-title" data-modal-title>
                {{ testimonialName }}</h4>

            <div data-modal-text>
                <p>
                    {{ testimonialText }}
                </p>
            </div>

            </div>

        </section>

        </div>


        <!--
        - clients
        -->

    </article>





    <!--
        - #RESUME
    -->

    <article class="resume" :class="{active: pageId == 'Resume'}" data-page="resume">

        <header>
        <h2 class="h2 article-title">Resume</h2>
        </header>

        <section class="timeline">

        <div class="title-wrapper">
            <div class="icon-box">
            <ion-icon name="book-outline"></ion-icon>
            </div>

            <h3 class="h3">Education</h3>
        </div>

        <ol class="timeline-list">

            <li class="timeline-item">

            <h4 class="h4 timeline-item-title">University of Hawaii - West Oahu</h4>

            <span>2015 — 2018</span>

            <p class="timeline-text">
                During my university, I focus on web development and artificial intelligence. I started my career as a software developer when I was at university and I tried myself to master programming languages and frameworks. As a result, I could get involved with some projects online and I got to know how to use github and how to develop web applications
            </p>

            </li>

        </ol>

        </section>

        <section class="timeline">

        <div class="title-wrapper">
            <div class="icon-box">
            <ion-icon name="book-outline"></ion-icon>
            </div>

            <h3 class="h3">Experience</h3>
        </div>

        <ol class="timeline-list">

            <li class="timeline-item">

                <h4 class="h4 timeline-item-title">Junior Full Stack Developer</h4>

                <span>2018 — 2020</span>

                <p class="timeline-text">
                    I worked as a junior full stack developer in Imagine WEB Creation. This company is based in Hawaii. During this time, I created 2 websites for society and developed my team-work skills by working in close-collaboration with 6 other students on github.
                </p>

            </li>

            <li class="timeline-item">

                <h4 class="h4 timeline-item-title">Full Stack Developer</h4>

                <span>2020 — 2022</span>

                <p class="timeline-text">
                    I worked as a full stack developer in Ikagai Technology Corporation. This company is based in Osaka. During this time, I developed a remote control system based on B/S architecture. Used C++ for agent and node.js for web server. Used SSL and certificate for security

                </p>

            </li>

        </ol>

        </section>

        <section class="skill">

        <h3 class="h3 skills-title">My skills</h3>

        <ul class="skills-list content-card">

            <li class="skills-item">

            <div class="title-wrapper">
                <h5 class="h5">Backend Development</h5>
                <data value="90">90%</data>
            </div>

            <div class="skill-progress-bg">
                <div class="skill-progress-fill" style="width: 90%;"></div>
            </div>

            </li>

            <li class="skills-item">

            <div class="title-wrapper">
                <h5 class="h5">Frontend Development</h5>
                <data value="70">70%</data>
            </div>

            <div class="skill-progress-bg">
                <div class="skill-progress-fill" style="width: 70%;"></div>
            </div>

            </li>

            <li class="skills-item">

            <div class="title-wrapper">
                <h5 class="h5">React Native</h5>
                <data value="90">90%</data>
            </div>

            <div class="skill-progress-bg">
                <div class="skill-progress-fill" style="width: 90%;"></div>
            </div>

            </li>

            <li class="skills-item">

            <div class="title-wrapper">
                <h5 class="h5">Artificial Intelligence</h5>
                <data value="50">50%</data>
            </div>

            <div class="skill-progress-bg">
                <div class="skill-progress-fill" style="width: 50%;"></div>
            </div>

            </li>

        </ul>

        </section>

    </article>





    <!--
        - #PORTFOLIO
    -->

    <article class="portfolio" :class="{active: pageId == 'Portfolio'}" data-page="portfolio">

        <header>
        <h2 class="h2 article-title">Portfolio</h2>
        </header>

        <section class="projects">

        <div class="filter-select-box">

            <button class="filter-select" data-select>

            <div class="select-value" data-selecct-value>Select category</div>

            <div class="select-icon">
                <ion-icon name="chevron-down"></ion-icon>
            </div>

            </button>

        </div>

        <ul class="project-list">

            <li class="project-item active" data-filter-item data-category="web development">
            <a href="https://azuki.com" target="_blank">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="../assets/images/project-1.jpg" alt="finance" loading="lazy">
                </figure>

                <h3 class="project-title">Azuki</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

            <li class="project-item active" data-filter-item data-category="web design">
            <a href="https://dsml.ru/" target="_blank">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="../assets/images/project-5.png" alt="dsm." loading="lazy">
                </figure>

                <h3 class="project-title">DSM.</h3>

                <p class="project-category">Web design</p>

            </a>
            </li>

            <li class="project-item active" data-filter-item data-category="web design">
            <a href="https://www.metaspark.io/" target="_blank">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="../assets/images/project-6.png" alt="metaspark" loading="lazy">
                </figure>

                <h3 class="project-title">MetaSpark</h3>

                <p class="project-category">Web design</p>

            </a>
            </li>

            <li class="project-item active" data-filter-item data-category="applications">
            <a href="https://www.dickssportinggoods.com/" target="_blank">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="../assets/images/project-8.jpg" alt="task manager" loading="lazy">
                </figure>

                <h3 class="project-title">Dick's Sporting Goods</h3>

                <p class="project-category">Applications</p>

            </a>
            </li>

            <li class="project-item active" data-filter-item data-category="web development">
            <a href="https://arrival.com/" target="_blank">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="../assets/images/project-9.png" alt="arrival" loading="lazy">
                </figure>

                <h3 class="project-title">Arrival</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

        </ul>

        </section>

    </article>
</template>