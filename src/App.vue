<script setup lang="ts">
import MaisonCard from './components/MaisonCard.vue'
import { type MaisonResponse, Collections } from './pocketbase-types'

const maisonsListe: MaisonResponse[] = [
  {
    adresse: 'rue test 90000 Belfort',
    collectionId: 'sidpkt9hmbfwoeb',
    collectionName: Collections.Maison,
    created: '2023-05-01 14:00:54.598Z',
    favori: true,
    id: '64l3n8nar836i5j',
    images: ['pexels_binyamin_mellish_106399_bnHdy6H03e.jpg'],
    nbChambres: 3,
    nbSdb: 2,
    nomMaison: 'alpha',
    prix: 252000,
    surface: 120,
    updated: '2023-05-01 14:00:54.598Z'
  },
  {
    adresse: 'Montbéliard',
    collectionId: 'sidpkt9hmbfwoeb',
    collectionName: Collections.Maison,
    created: '2023-05-01 14:01:25.740Z',
    favori: false,
    id: '2bubgl4tmljx5q4',
    images: [],
    nbChambres: 2,
    nbSdb: 1,
    nomMaison: 'beta',
    prix: 239000,
    surface: 100,
    updated: '2023-05-01 14:01:25.740Z'
  },
  {
    adresse: 'Belfort',
    collectionId: 'sidpkt9hmbfwoeb',
    collectionName: Collections.Maison,
    created: '2023-05-01 14:01:56.650Z',
    favori: true,
    id: 'yxui4b61ovt1nct',
    images: [],
    nbChambres: 5,
    nbSdb: 2,
    nomMaison: 'gamma',
    prix: 320000,
    surface: 142,
    updated: '2023-05-01 14:01:56.650Z'
  }
]
console.log(maisonsListe)
</script>

<template>
  <header>
    <h1 class="text-4xl">Test</h1>
  </header>

  <main>
    <MaisonCard v-for="uneMaison of maisonsListe" :v-key="uneMaison.id" v-bind="uneMaison" />
  </main>
</template>
