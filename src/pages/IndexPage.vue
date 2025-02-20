<template>
  <q-page class="">
    <div class="q-col-gutter-md row items-start">
      <div class="col-12">
        <q-img src="/images/cover2.png">
        </q-img>
      </div>
    </div>
    
    <div class=" q-mx-xl q-py-xl">
      <!--Tendances-->
      <div class="text-h3 q-px-md q-py-md text-primary">Tendances</div>
      <div class="row">
        <div class="col-6 q-pa-md">
          <q-img src="/images/product1.jpg" :ratio="1">
            <div class="absolute-bottom bg-info" style="">
              <div class="q-px-sm text-h5">Robe Amber</div>
              <div class="q-pa-sm">Eclat doré du crépuscule, drapant la silhouette d’une lueur envoûtante.</div>
            </div>
          </q-img>
        </div>
        <div class="col-6 q-pa-md">
          <q-img src="/images/product2.jpg" :ratio="1">
            <div class="absolute-bottom bg-info">
              <div class="q-px-sm text-h5">Robe Amber</div>
              <div class="q-pa-sm">Eclat doré du crépuscule, drapant la silhouette d’une lueur envoûtante.</div>
            </div>
          </q-img>
        </div>
        <div class="col-6 q-pa-md">
          <q-img src="/images/product4.jpg" :ratio="1">
            <div class="absolute-bottom bg-info">
              <div class="q-px-sm text-h5">Robe Amber</div>
              <div class="q-pa-sm">Eclat doré du crépuscule, drapant la silhouette d’une lueur envoûtante.</div>
            </div>
          </q-img>
        </div>
        <div class="col-6 q-pa-md">
          <q-img src="/images/product6.jpg" :ratio="1">
            <div class="absolute-bottom bg-info">
              <div class="q-px-sm text-h5">Robe Amber</div>
              <div class="q-pa-sm">Eclat doré du crépuscule, drapant la silhouette d’une lueur envoûtante.</div>
            </div>
          </q-img>
        </div>
      </div>
      <!--Nouveaux-->
      <div class="text-h3 q-px-md q-py-md text-primary q-mt-xl">Nouveaux</div>
      <div class="q-py-md row">
        <div class="col-4 q-px-md">
          <q-img src="/images/product7.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="/images/product5.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="/images/product8.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
      </div>
    </div>

    
    <div class="q-col-gutter-md row items-start">
      <div class="col-12">
        <q-img src="/images/cover1.png">
        </q-img>
      </div>
    </div>

    
    <div class=" q-mx-xl q-py-xl">
      
      <!--Populaire-->
      <div class="text-h3 q-px-md q-py-md text-primary q-mt-xl">Populaire</div>
      <div class="q-py-md row">
        <div class="col-4 q-px-md">
          <q-img src="/images/product4.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="/images/product2.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
        <div class="col-4 q-px-md">
          <q-img src="/images/product5.jpg" :ratio="5/6">
          </q-img>
            <div class="q-py-md text-h5 text-primary">Robe Amber</div>
            <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" />
        </div>
      </div>
    </div>

    <q-carousel
        v-model="slide"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="800px"
        class="bg-primary text-white shadow-1 rounded-borders"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center" >
          <q-img src="/images/temoin1.jpg" class="q-my-md" height="400px" width="400px"/>
          <div class="text-center text-h4">Emma</div>
          <div class="q-my-xl text-center text-h5" style="max-width: 600px;">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="lucie" class="column no-wrap flex-center" >
          <q-img src="/images/temoin1.jpg" class="q-my-md" height="400px" width="400px"/>
          <div class="text-center text-h4">Lucie</div>
          <div class="q-my-xl text-center text-h5" style="max-width: 600px;">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="sara" class="column no-wrap flex-center" >
          <q-img src="/images/temoin1.jpg" class="q-my-md" height="400px" width="400px"/>
          <div class="text-center text-h4">Sara</div>
          <div class="q-my-xl text-center text-h5" style="max-width: 600px;">
            {{ lorem }}
          </div>
        </q-carousel-slide>
      </q-carousel>

  </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('style'),
      lorem: "C'est ma boutique préférée pour trouver des pièces uniques et stylées. Je trouve toujours quelque chose qui correspond parfaitement à mon style. Leur service client est également incroyablement attentionné."
    }
  }
}
</script>

<style scoped>
.custom-footer {
  font-family: 'Poppins', sans-serif;
}
</style>