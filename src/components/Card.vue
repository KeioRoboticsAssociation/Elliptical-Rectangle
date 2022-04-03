<template>
  <div class="card">
    <div class="card-body">
      <a :href="`//www.orientation.keio-students.jp/circle/${club.id}`">
        <div class="imgBoxInner">
          <img :src="`${club.image}`" loading="lazy" />
        </div>
        <div class="discription">
          <div class="discription">
            <h5 class="card-text">{{ club.title }}</h5>
            <ul>
              <li>
                キャンパス:
                <div class="chip" v-for="(place) in props.club.places" :key="place">
                  {{ place }}
                  <!-- <span v-if="index != props.club.campuses.length">,</span> -->
                </div>
              </li>
              <!--<li>
                          タグ:
                          <div class="chip" v-for='tag in videoinfo.tags'>{{tag}}</div>
              </li>-->
            </ul>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

export type Club = {
  title: string,
  id: number,
  places: string[],
  image: string
}

interface Props {
  club: Club
}

const props = defineProps<Props>()

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~mdb-ui-kit/css/mdb.min.css";
.discription {
  padding: 2% 2%;
}
</style>
