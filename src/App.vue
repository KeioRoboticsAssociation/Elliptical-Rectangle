<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-white row justify-content-between">
    <h1>Circle Square(Alternative)</h1>
  </nav>
  <div class="col-12">
    <div id=" app" class="row cards" style="padding:0 50px; margin: 10px 0 0 0">
      <div class="row">
        <div class="col-md-4" v-for="club in data" :key="club.url">
          <Card :club="club"></Card>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Card, { Club } from './components/Card.vue'
import * as mdb from 'mdb-ui-kit' // lib
import { Input } from 'mdb-ui-kit' // module

const data: Club[] = [
  {
    name: '将棋研究会',
    url: '2',
    campuses: ['日吉']
  },
  {
    name: 'ワグネル・ソサィエティー男声合唱団',
    url: '3',
    campuses: ['日吉', '三田']
  },
  {
    name: '塾生総合研究所',
    url: '4',
    campuses: ['日吉']
  },
  {
    name: '貘之會',
    url: '5',
    campuses: ['日吉']
  },
  {
    name: 'Twinkles',
    url: '6',
    campuses: ['日吉']
  },
  {
    name: '無線工学研究会',
    url: '7',
    campuses: ['日吉']
  },
  {
    name: '塾生会館運営委員会',
    url: '8',
    campuses: ['日吉']
  },
  {
    name: 'SFC CLIP',
    url: '9',
    campuses: ['日吉']
  },
  {
    name: 'アルティメットサークル ホワイトホーンズ',
    url: '10',
    campuses: ['日吉']
  },
  {
    name: '',
    url: '',
    campuses: ['日吉']
  }
]
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600&family=Noto+Sans+JP:wght@400;700&display=swap");
* {
  font-family: "Inter", "Noto Sans JP", sans-serif;
}

* {
  font-family: Inter, "Noto Sans JP", sans-serif;
}

.cards {
  display: flex;
}
.card {
  margin: 10px;
  padding: 0;
}

.card-body {
  padding: 0;
}

.discription {
  padding: 2% 8%;
}

iframe {
  width: 100%;
  height: auto;
  aspect-ratio: 16/9;
}

ul {
  list-style-type: none;
  padding: 0;
}

#addbutton {
  position: fixed;
  bottom: 2%;
  right: 2%;
}

nav {
  width: 100%;
  margin: 0;
}

.form-outline {
  margin: 10px;
}

.previewBox {
  width: 100%;
  height: auto;
  aspect-ratio: 16/9;
  text-align: center;
  display: inline-block;
  vertical-align: middle;
}

body {
  width: 99%;
}

.chip {
  display: inline-block;
  padding: 2px 10px;
  margin: 0 5px;
  border-radius: 20px;
  background-color: #d6d6d6;
}

a {
  color: rgb(87, 87, 87);
}

a:hover {
  color: rgb(146, 146, 146);
}
</style>
