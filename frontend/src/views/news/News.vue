<template>
  <v-container fluid>
    <v-card class="ma-3 pa-3">
      <v-card-title primary-title>
        <div class="headline primary--text">{{getTitle}}</div>
      </v-card-title>
      <v-card-text>
        <div class="headline font-weight-light ma-5"><vue-markdown>{{getContent}}</vue-markdown></div>
      </v-card-text>
      <v-card-actions>
        <v-btn to="/main/news/edit">Editar Noticia</v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { Store } from 'vuex';

@Component
export default class News extends Vue {


  get getTitle() {
    return "Una noticia maravillosa"
  }
  
  get getContent() {
    const text = "#un contenido asombroso\n La mejor parte del contenido asombroso es lo **asombroso** que es";

    return text;
  }
}
</script>