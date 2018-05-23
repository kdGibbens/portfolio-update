<template>
  <div class="portfolio">
    <div class="portfolio-projects">
      <div class="recent project-section">
        <h2>{{recent}}</h2>
        <a class="project-link" v-for="project in portfolio" v-bind:key="project.id" v-bind:href="project.url" v-if="!project.internal && project.new" target="_blank">
          <div class="card">
            <font-awesome-icon :icon="[project.fa, project.icon]" class="icon" />
            <h3>{{ project.name }}</h3>
          </div>
        </a>
        <nuxt-link class="project-link" :id="project.id" :to="project.url" v-bind:key="project.id" v-else-if="project.internal && project.new">
          <div class="card">
            <font-awesome-icon :icon="[project.fa, project.icon]" class="icon" />
            <h3>{{ project.name }}</h3>
          </div>
        </nuxt-link>
      </div>

      <div class="older project-section">
        <h2>{{older}}</h2>
        <a class="project-link" v-for="project in portfolio" v-bind:key="project.id" v-bind:href="project.url" v-if="!project.new" target="_blank">
          <div class="card">
            <font-awesome-icon :icon="[project.fa, project.icon]" class="icon" />
            <h3>{{ project.name }}</h3>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
      data() {
        return {
          older: 'Older Projects:',
          recent: 'Recent Projects:',
          portfolio: {
            oblique: {
              id: 'oblique',
              name: 'Oblique Strategies',
              url: 'https://hungry-lumiere-800fda.netlify.com/',
              internal: false,
              new: true,
              fa: 'fas',
              icon: 'bomb'
            },
            nasa: {
              id: 'nasa',
              name: 'Nasa Image Search',
              url: 'https://suspicious-poitras-5781ff.netlify.com/',
              internal: false,
              new: true,
              fa: 'fas',
              icon: 'space-shuttle'
            },
            crypto: {
              id: 'crypto',
              name: 'Crypto Price Watch',
              url: 'https://gracious-khorana-24625a.netlify.com/',
              internal: false,
              new: true,
              fa: 'fab',
              icon: 'bitcoin'
            },
            translator: {
              id: 'Language',
              name: 'Language Translator',
              url: 'https://reverent-goldberg-266107.netlify.com/#/',
              internal: false,
              new: true,
              fa: 'fas',
              icon: 'language'
            },
            speechToText: {
              id: 'speechToText',
              name: 'Speech to Text',
              url: 'https://vibrant-ritchie-6861ef.netlify.com/',
              internal: false,
              new: false,
              fa: 'far',
              icon: 'comment'
            },
            quote: {
              id:'Quote',
              name: 'Quote Machine',
              url: 'http://kellygibbens.com/ht_docs/random_quote_machine_jquery/',
              internal: false,
              new: false,
              fa: 'fas',
              icon: 'quote-right'
            },
            explore: {
              id: 'explore',
              name: 'Explore Outdoors',
              url: 'http://exploreoutdoors.us/',
              internal: false,
              new: false,
              fa: 'fas',
              icon: 'tree'
            },
          }
        }
      }
    }
</script>