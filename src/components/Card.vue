<template></template>
    <div class="card">
        <div class="card-body">
            <div class="discription">
                <h5 class="card-text"><a :href="`//www.orientation.keio-students.jp/circle/${club.url}`">{{club.name}}</a></h5>
                <ul>
                    <li>キャンパス:
                      <div class="chip" v-for="(campus) in props.club.campuses" :key="campus">{{campus}}
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
    </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

export type Campuses = 'オンライン' | '三田' | '日吉' | '矢上' | '湘南藤沢'| '信濃町'| '芝共立'
export type Club = {
  name : string,
  url: string,
  campuses: Campuses[]
}
interface Props {
  club: Club
}

const props = defineProps<Props>()

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~mdb-ui-kit/css/mdb.min.css';
</style>
