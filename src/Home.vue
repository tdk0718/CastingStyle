<template>
<feed_kind></feed_kind>
  <v-ons-page>
    <h2 class="recommend_talent main_title">注目のタレント<span class="more_bot">もっと見る</span></h2>
    <ul class="reccomend_talent">
    <li></li>
    
    </ul>

    <h2 class="each_cate main_title">カテゴリ別<span class="more_bot">もっと見る</span></h2>
    <table classtalent_cate>
      <tr><td></td><td></td></tr>
      <tr><td></td><td></td></tr>
      <tr><td></td><td></td></tr>
    </table>


    <h2 class="reccent_taleny main_title">最近チェックしたタレント<span class="more_bot">もっと見る</span></h2>
  </v-ons-page>
</template>

<style>
span.more_bot {
    font-size: 10px;
    float: right;
    font-weight: 500;
}

.page__content h2 {
    font-size: 14px;
    width: 95%;
    margin: 10px auto;
    font-weight: 900;
}

</style>

<script>

import feed_kind from "./feed_kind"
  
  export default {
    compornents:{feed_kind},
    template:"<feed_kind></feed_kind>",
    data: {
     
    },
    methods: {
      
     
    },
    computed: {
      
    },
    
  }






<script>