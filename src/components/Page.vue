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
    <article class="about" :class="{active: pageId == 'About'}" data-page="about">

        <header>
        <h2 class="h2 article-title">About me</h2>
        </header>

        <section class="about-text">
        <p>
            I'm a creative developer from Serpukhov, Russia. I'm a fullstack developer and mobile app developer. I'm also familiar with ai and I have experience with VGG16 and VGG19.
        </p>

        <p>
            My job is to build responsive websites for clients to satisfy their demands. I carry out clients' orders for 100% and I add my personal creative opinions for the success of the project. After development, I even add some additional maintenance service for clients so they can easily learn how it works.
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
            <div class="content-card" data-testimonials-item>

                <figure class="testimonials-avatar-box">
                <img src="../assets/images/avatar-1.png" alt="Daniel lewis" width="60" data-testimonials-avatar>
                </figure>

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Edward Johnson</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav was hired to create a remote control system for me. He showed himself as a gifted developer and did his best to satisfy my demands. He is a talented backend developer and creative front-end designer. He is very friendly and cool, a client-friendly developer. I look forward to working with him further.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" data-testimonials-item>

                <figure class="testimonials-avatar-box">
                    <img src="../assets/images/avatar-2.png" alt="Jessica miller" width="60" data-testimonials-avatar>
                </figure>

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Hadi Mashhour</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav showed a good skill of project management and maintenance. He is a database expert and he is really good at debugging. He solved our site's problem perfectly. Looking forward to working with him again.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" data-testimonials-item>

                <figure class="testimonials-avatar-box">
                    <img src="../assets/images/avatar-3.png" alt="Emily evans" width="60" data-testimonials-avatar>
                </figure>

                <h4 class="h4 testimonials-item-title" data-testimonials-title>Venkat Muhammad</h4>

                <div class="testimonials-text" data-testimonials-text>
                <p>
                    Viacheslav worked on a small project using google search api. He showed himself as a good view of programming and introduced me to the world of apis. He is a good developer and really client-friendly. Looking forward to working with him again.
                </p>
                </div>

            </div>
            </li>

            <li class="testimonials-item">
            <div class="content-card" data-testimonials-item>

                <figure class="testimonials-avatar-box">
                    <img src="../assets/images/avatar-4.png" alt="Henry william" width="60" data-testimonials-avatar>
                </figure>

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

        <div class="modal-container" data-modal-container>

        <div class="overlay" data-overlay></div>

        <section class="testimonials-modal">

            <button class="modal-close-btn" data-modal-close-btn>
            <ion-icon name="close-outline"></ion-icon>
            </button>

            <div class="modal-img-wrapper">
            <figure class="modal-avatar-box">
                <img src="./assets/images/avatar-1.png" alt="Daniel lewis" width="80" data-modal-img>
            </figure>

            <img src="./assets/images/icon-quote.svg" alt="quote icon">
            </div>

            <div class="modal-content">

            <h4 class="h3 modal-title" data-modal-title>Daniel lewis</h4>

            <div data-modal-text>
                <p>
                Richard was hired to create a corporate identity. We were very pleased with the work done. She has a
                lot of experience
                and is very concerned about the needs of client. Lorem ipsum dolor sit amet, ullamcous cididt
                consectetur adipiscing
                elit, seds do et eiusmod tempor incididunt ut laborels dolore magnarels alia.
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

            <h4 class="h4 timeline-item-title">MBOU secondary school No. 10</h4>

            <span>2007 - 2013</span>

            <p class="timeline-text">
                I studied at MBOU secondary school No. 10 in Serpukhov and graduated with a B.
            </p>

            </li>

            <li class="timeline-item">

            <h4 class="h4 timeline-item-title">Moskovskiy Universitet Imeni S.yu. Vitte</h4>

            <span>2014 — 2017</span>

            <p class="timeline-text">
                I studied at Moskovskiy Universitet Imeni S.yu. Vitte. I studied software engineering there for 3 years and graduated with a B.
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

            <h4 class="h4 timeline-item-title">Creative developer</h4>

            <span>2018 — 2022</span>

            <p class="timeline-text">
                I worked as a junior developer in KOTELOV. During this time I contact some clients and got some good reviews for their projects.
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
                <data value="80">90%</data>
            </div>

            <div class="skill-progress-bg">
                <div class="skill-progress-fill" style="width: 80%;"></div>
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

        <ul class="filter-list">

            <li class="filter-item">
            <button class="active" data-filter-btn>All</button>
            </li>

            <li class="filter-item">
            <button data-filter-btn>Web design</button>
            </li>

            <li class="filter-item">
            <button data-filter-btn>Applications</button>
            </li>

            <li class="filter-item">
            <button data-filter-btn>Web development</button>
            </li>

        </ul>

        <div class="filter-select-box">

            <button class="filter-select" data-select>

            <div class="select-value" data-selecct-value>Select category</div>

            <div class="select-icon">
                <ion-icon name="chevron-down"></ion-icon>
            </div>

            </button>

            <ul class="select-list">

            <li class="select-item">
                <button data-select-item>All</button>
            </li>

            <li class="select-item">
                <button data-select-item>Web design</button>
            </li>

            <li class="select-item">
                <button data-select-item>Applications</button>
            </li>

            <li class="select-item">
                <button data-select-item>Web development</button>
            </li>

            </ul>

        </div>

        <ul class="project-list">

            <li class="project-item  active" data-filter-item data-category="web development">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-1.jpg" alt="finance" loading="lazy">
                </figure>

                <h3 class="project-title">Azuki</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web development">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-2.png" alt="orizon" loading="lazy">
                </figure>

                <h3 class="project-title">Anthobexitsolutions</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web design">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-3.jpg" alt="fundo" loading="lazy">
                </figure>

                <h3 class="project-title">Anthobexitsolutions</h3>

                <p class="project-category">Web design</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="applications">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-4.png" alt="brawlhalla" loading="lazy">
                </figure>

                <h3 class="project-title">Whole Foods Market</h3>

                <p class="project-category">Applications</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web design">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-5.png" alt="dsm." loading="lazy">
                </figure>

                <h3 class="project-title">DSM.</h3>

                <p class="project-category">Web design</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web design">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-6.png" alt="metaspark" loading="lazy">
                </figure>

                <h3 class="project-title">MetaSpark</h3>

                <p class="project-category">Web design</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web development">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-7.png" alt="summary" loading="lazy">
                </figure>

                <h3 class="project-title">Intricategroup</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="applications">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-8.jpg" alt="task manager" loading="lazy">
                </figure>

                <h3 class="project-title">Dick's Sporting Goods</h3>

                <p class="project-category">Applications</p>

            </a>
            </li>

            <li class="project-item  active" data-filter-item data-category="web development">
            <a href="#">

                <figure class="project-img">
                <div class="project-item-icon-box">
                    <ion-icon name="eye-outline"></ion-icon>
                </div>

                <img src="./assets/images/project-9.png" alt="arrival" loading="lazy">
                </figure>

                <h3 class="project-title">Arrival</h3>

                <p class="project-category">Web development</p>

            </a>
            </li>

        </ul>

        </section>

    </article>
</template>