<script setup lang="ts">
import ContactSection from './components/ContactSection.vue';
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import ProjectCard from './components/ProjectCard.vue';

import DataStorypng from './assets/DataStoryOnTrainDelays.png';
import DateIdeapng from './assets/DateIdeaFinder.png';
import RiggedMotionpng from './assets/RiggedMotionStudio.png';

function useDocumentMeta() {
  const setTitle = (title: string) => {
    document.title = title;
  };

  const setDescription = (content: string) => {
    let meta = document.querySelector('meta[name="description"]');
    if (!meta) {
      meta = document.createElement('meta');
      meta.setAttribute('name', 'description');
      document.head.appendChild(meta);
    }
    meta.setAttribute('content', content);
  };

  return {
    setTitle,
    setDescription
  };
}

const { setTitle, setDescription } = useDocumentMeta();

setTitle('Portfolio Juliette Kauflin');
setDescription('Hierbei handelt es sich um einen überblick dreier meiner besten Websiten, welche ich bis und mit stand Januar 2025 erstellt habe, soll dazu dienen, dass ich diesen anhängen kann bei der Bewerbung für eine Stelle in den Bereichen design, Webdesign und Webentwicklung');
</script>

<template>
  <div class="min-h-screen flex flex-col bg-white w-full m-0">
    <Header />
    <HeroSection />
    <main class="container mx-auto space-y-24">
      <section id="projects" class="mx-auto py-24 space-y-24">
        <h2 class="text-3xl font-bold text-purple-600 px-6 mb-12 text-left">Meine Projekte</h2>
        <ProjectCard
          title="Data Story on Train Delays"
          description="Zugverspätung & Wetter ist eine Webanwendung, die analysiert, wie sich die Wetterbedingungen auf Zugverspätungen in der Schweiz auswirken. Benutzer können interaktive Diagramme und Schlüsselstatistiken erforschen, um Muster und Korrelationen aufzudecken, die Einblicke für Pendler und Planer bieten."
          :tags="['MariaDB', 'Tailwind CSS', 'Chart.js', 'APIs']"
          :image="DataStorypng"
          link="https://train-delay.juka.dev/"
          github="https://github.com/JuKa2023/im3-train-delay-analysis"
        />
        <ProjectCard
          title="Date Idea Finder"
          description="Date Idea ist eine Webanwendung, die Nutzern hilft, auf ihre Vorlieben zugeschnittene Verabredungsideen zu finden. Egal, ob Sie nach einem romantischen Abendessen, einem abenteuerlichen Ausflug oder einem gemütlichen Abend zu Hause suchen, Date Idea hat alles für Sie."
          :tags="['Vue.js', 'Supabase']"
          :image="DateIdeapng"
          link="https://juka2023.github.io/date-finder/"
          github="https://github.com/JuKa2023/date-finder"
        />
        <ProjectCard
          title="Rigged-Motion-Studios"
          description="Rigged-Motion-Studios ist eine Website für meine Mitstudenten, die ein Start-up gründen wollen. Sie dient als digitale Visitenkarte, veranschaulicht ihre Arbeit und startet ihr erstes Produkt über eine Versteigerung. Ein 3D-animiertes Werbevideo mit außerirdischem Thema präsentiert ein Platzhalterobjekt, das nach der Auktion durch das Produkt des Höchstbietenden ersetzt wird. Ziel ist es, das Start-up bekannt zu machen und erste Kunden zu gewinnen."
          :tags="['ShadCN', 'Vue.js', 'Supabase']"
          :image="RiggedMotionpng"
          link="https://rigged-motion.com/#/"
          github="https://github.com/JuKa2023/rigged-motion-web"
        />
      </section>
    </main>
    <ContactSection id="contact" />
  </div>
</template>
