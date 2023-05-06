<script setup lang="ts">
import MaisonCard from './components/MaisonCard.vue'
import { Collections, type MaisonResponse } from './pocketbase-types'
const maisonsListe = [
  {
    adresse: '123 rue de la Paix, Villefranche-sur-Mer',
    collectionId: 'cb6ykzaxavlbmps',
    collectionName: Collections.Maison,
    created: '2023-04-28 11:56:35.046Z',
    favori: true,
    id: 'ygxq282h5qv5ytx',
    images: ['pexels_fomstock_com_1115804_Gw8zvePG5y.jpg'],
    nbChambres: 4,
    nbSdb: 3,
    nomMaison: 'Villa Paradis',
    prix: 1800000,
    surface: 300,
    updated: '2023-04-28 11:57:08.746Z'
  },
  {
    adresse: '55 chemin des Érables, Megève',
    collectionId: 'cb6ykzaxavlbmps',
    collectionName: Collections.Maison,
    created: '2023-04-28 11:57:55.943Z',
    favori: false,
    id: 'cskxdbof5culkj2',
    images: ['pexels_julia_kuzenkov_1974596_WFypIPL8Vs.jpg'],
    nbChambres: 3,
    nbSdb: 2,
    nomMaison: 'Chalet du Lac',
    prix: 750000,
    surface: 180,
    updated: '2023-04-28 11:57:55.943Z'
  },
  {
    adresse: '17 avenue des Pins, Saint-Tropez',
    collectionId: 'cb6ykzaxavlbmps',
    collectionName: Collections.Maison,
    created: '2023-04-28 11:58:42.996Z',
    favori: true,
    id: 'uvgjyjk5owraubc',
    images: ['pexels_zoe_koskinioti_2183521_lEy2QraDIq.jpg'],
    nbChambres: 5,
    nbSdb: 4,
    nomMaison: 'Maison de la Colline',
    prix: 1100000,
    surface: 450,
    updated: '2023-04-28 11:58:42.996Z'
  },
  {
    adresse: '24 rue de la Liberté, Lyon',
    collectionId: 'cb6ykzaxavlbmps',
    collectionName: Collections.Maison,
    created: '2023-04-28 12:00:10.890Z',
    favori: false,
    id: 'u8sh8n9decfrl5y',
    images: ['pexels_valeriia_miller_2587054_Zhu2gvCVgB.jpg'],
    nbChambres: 2,
    nbSdb: 1,
    nomMaison: 'Appartement de la Tour',
    prix: 320000,
    surface: 80,
    updated: '2023-04-28 12:00:10.890Z'
  },
  {
    adresse: '1 avenue des Palmiers, Cannes',
    collectionId: 'cb6ykzaxavlbmps',
    collectionName: Collections.Maison,
    created: '2023-04-28 12:00:43.283Z',
    favori: true,
    id: '55wgbngz9010q42',
    images: ['pexels_scott_webb_1022936_whraGuS0f1.jpg'],
    nbChambres: 6,
    nbSdb: 5,
    nomMaison: 'Villa de la Mer',
    prix: 3200000,
    surface: 600,
    updated: '2023-04-28 12:00:43.283Z'
  }
]
</script>
<template>
  <div>
    <h1>Test</h1>

    <MaisonCard v-bind="maisonsListe[0]" />
  </div>
</template>
