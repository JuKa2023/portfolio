clea<script setup lang="ts">

useHead({
  title: 'Portfolio Juliette Kauflin',
  meta: [
    { name: 'description', content: 'Hierbei handelt es sich um einen überlick drei meiner besten Wbeseiten, welche ich bis und mit stand Januar 2025 erstellt habe, soll dazu dienen, dass ich diesen anhängen kann bei der Bewerbung für eine Stelle in den Bereichen design, Webdesign und Webentwicklung' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [ { innerHTML: 'console.log(\'Hello world\')' } ]
})

import ContactSection from './components/ContactSection.vue';
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import ProjectCard from './components/ProjectCard.vue';
import DataStorypng from './assets/DataStoryOnTrainDelays.png';
import DateIdeapng from './assets/DateIdeaFinder.png';
import RiggedMotionpng from './assets/RiggedMotionStudio.png';

</script>

<template>
  <div>
    <Header />
    <HeroSection />
    <main class="container mx-auto px-6 space-y-24">
      <ProjectCard
        title="Data Story on Train Delays"
        description="Zugverspätung & Wetter ist eine Webanwendung, die analysiert, wie sich die Wetterbedingungen auf Zugverspätungen in der Schweiz auswirken. Benutzer können interaktive Diagramme und Schlüsselstatistiken erforschen, um Muster und Korrelationen aufzudecken, die Einblicke für Pendler und Planer bieten."
        :tags="['MariaDB', 'Tailwind CSS', 'Chart.js', 'APIs']"
        :image="DataStorypng"
        link="https://im3julie.rigged-motion.com/"
      />
      <ProjectCard
        title="Date Idea Finder"
        description="Date Idea ist eine Webanwendung, die Nutzern hilft, auf ihre Vorlieben zugeschnittene Verabredungsideen zu finden. Egal, ob Sie nach einem romantischen Abendessen, einem abenteuerlichen Ausflug oder einem gemütlichen Abend zu Hause suchen, Date Idea hat alles für Sie."
        :tags="['Vue.js', 'Supabase']"
        :image="DateIdeapng"
        link="https://juka2023.github.io/date-finder/"
      />
      <ProjectCard
        title="Rigged-Motion-Studios"
        description="Rigged-Motion-Studios ist eine Website für meine Mitstudenten, die ein Start-up gründen wollen. Sie dient als digitale Visitenkarte, veranschaulicht ihre Arbeit und startet ihr erstes Produkt über eine Versteigerung. Ein 3D-animiertes Werbevideo mit außerirdischem Thema präsentiert ein Platzhalterobjekt, das nach der Auktion durch das Produkt des Höchstbietenden ersetzt wird. Ziel ist es, das Start-up bekannt zu machen und erste Kunden zu gewinnen."
        :tags="['ShadCN', 'Vue.js', 'Supabase']"
        :image="RiggedMotionpng"
        link="https://rigged-motion.com/#/"
      />
    </main>
    <ContactSection id="contact" />
    <Footer />
  </div>
</template>
