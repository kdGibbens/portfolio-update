<template>
  <div class="portfolio">
    <div class="protfolio-projects">
      <div class="recent">
        <h2>{{recent}}</h2>

        <a v-for="project in portfolio" v-bind:key="project.id" v-bind:href="project.url" v-if="!project.internal && project.new" target="_blank">
          <div class="card">
            <h3>{{ project.name }}</h3>
          </div>
        </a>

        <nuxt-link v-bind:key="project.id" v-else-if="project.internal && project.new">
          <div class="card">
            <h3>{{ project.name }}</h3>
          </div>
        </nuxt-link>

      </div>

      <div class="older">
        <h2>{{older}}</h2>
        <a v-for="project in portfolio" v-bind:key="project.id" v-bind:href="project.url" v-if="!project.new" target="_blank">
          <div class="card">
            <h3>{{ project.name }}</h3>
          </div>
        </a>
      </div>
    <!-- <a v-for="project in portfolio" v-bind:key="project.id" v-bind:href="project.url" v-if="!project.internal" target="_blank">
      <div class="card">
        <h3>{{ project.name }}</h3>
      </div>
    </a> -->
    <!-- <nuxt-link v-bind:key="project.id" v-else>
      <div class="card">
        <h3>{{ project.name }}</h3>
      </div>
    </nuxt-link> -->
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
            crypto: {
              id: 'crypto',
              name: 'Crypto Price Watch',
              url: 'https://gracious-khorana-24625a.netlify.com/',
              internal: false,
              new: true
            },
            translator: {
              id: 'Language',
              name: 'Language Translator',
              url: 'https://reverent-goldberg-266107.netlify.com/#/',
              internal: false,
              new: true
            },
            quote: {
              id:'Quote',
              name: 'Quote Machine',
              url: 'http://kellygibbens.com/ht_docs/random_quote_machine_jquery/',
              internal: false,
              new: false
            },
            explore: {
              id: 'explore',
              name: 'Explore Outdoors',
              url: 'http://exploreoutdoors.us/',
              internal: false,
              new: false
            },
            scroll: {
              id: 'Scroll',
              name: 'Scroll Magic',
              url: 'http://kellygibbens.com/ht_docs/scrollMagic/',
              internal: false,
              new: false
            },
            pawn: {
              id: 'Pawn',
              name: 'Mission Pawn',
              url: 'http://missionpawn.com/',
              internal: false,
              new: false
            }
          }
        }
      }
    }
</script>