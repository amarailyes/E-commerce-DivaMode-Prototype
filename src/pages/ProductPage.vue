<template>
    <q-page class="">
        <div class="q-col-gutter-md row items-start">
            <div class="col-12 row q-pt-xl" style="max-width : 1000px; margin:auto">
                <div class="row col-12 q-py-md">
                    <div class="col-6 q-px-md">
                        <div class="q-pa-md" style="max-width:400px;margin:auto">
                            <q-carousel
                            swipeable
                            animated
                            v-model="slide"
                            thumbnails
                            infinite
                            height = "630px"
                            class="bg-secondary"
                            style="padding-bottom: 130px;"
                            >
                                <q-carousel-slide :name="1" img-src="/images/product4.jpg"  />
                                <q-carousel-slide :name="2" img-src="/images/product3.jpg" />
                            </q-carousel>
                        </div>
                    </div>
                    <div class="col-6">
                        <div class="text-h4 q-pb-xl text-primary q-mt-xl">Jupe portefeuille</div>
                        <p>Élégante et fluide, la jupe portefeuille sublime la silhouette avec son drapé délicat et son jeu d’asymétrie raffiné.</p>
                        <div class="q-pa-sm rounded-borders" >
                            Taille : 
                            <q-option-group
                            name="preferred_genre"
                            v-model="preferred"
                            :options="options"
                            color="primary"
                            inline
                            />
                        </div>
                        <div class="q-ma-md">
                            Couleur : <br>
                            <q-btn-toggle
                            v-model="Bordeau"
                            toggle-color="grey-7"
                            :options="colorOptions"
                            unelevated
                            style="background: #412e17;"
                            class="color-picker"
                            
                            />
                            <q-btn-toggle
                            v-model="Bordeau"
                            toggle-color="grey-7"
                            :options="colorOptions"
                            unelevated
                            style="background: #094832;"
                            class="color-picker q-ma-md"
                            
                            />
                            <q-btn-toggle
                            v-model="Bordeau"
                            toggle-color="grey-7"
                            :options="colorOptions"
                            unelevated
                            style="background: #7d0d30;"
                            class="color-picker"
                            
                            />
                        </div>
                        <q-btn unelevated color="primary" icon="add" label="Ajouter au panier" class="q-mt-xl"/>
                    </div>
                </div>
            </div>
            
            <!--similaires-->
            <div class="col-12  row" style="max-width : 1000px; margin:auto">
                <div class="col-12 q-py-md">
                    <div class="text-h3 q-px-md q-py-md text-primary q-mt-xl">Produits similaires</div></div>
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
    </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
        slide: ref(1),
        preferred: ref('s'),
        options: [
        {
        label: 'XS',
        value: 'xs'
        },
        {
        label: 'S',
        value: 's'
        },
        {
        label: 'M',
        value: 'm'
        },
        {
        label: 'L',
        value: 'l'
        },
        {
        label: 'XL',
        value: 'xl'
        }
        ],
        selectedColor : ref('red'),
        colorOptions : [
            { value: 'red', slot: 'red' }
        ],
    }
  }
}
</script>

<style>
.q-carousel__thumbnail{
    height : 100px!important;
}

.color-picker :deep(.q-btn) {
  width: 35px;
  height: 35px;
  margin: 4px;
  border-radius: 8px; /* Carré arrondi */
}

/* Personnalise chaque carré selon la couleur */
.color-picker :deep(.q-btn[aria-pressed="true"]) {
  border: 3px solid black; /* Bordure pour l'option sélectionnée */
}

/* Applique les couleurs */
[color="red"] { background: red; }
[color="blue"] { background: blue; }
[color="green"] { background: green; }
[color="yellow"] { background: yellow; }

</style>