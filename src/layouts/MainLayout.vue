<template>
  <q-layout view="lHh Lpr lFf">
    <!--TOOLBAR-->
    <q-header unelevated>
      <q-toolbar class="font-catana">
        <q-toolbar-title >
          <div class="text-h4 font-fleur">Diva Mode</div>
        </q-toolbar-title>

        <q-btn-toggle
          v-model="onglet_model"
          flat stretch
          class = "text-info"
          toggle-color="white"
          :options="onglet_options"
        />
        <q-space/>
        <q-icon class="q-mx-sm" name="mdi-instagram" color="secondary" size="sm"/>
        <q-icon class="q-mx-sm" name="mdi-facebook" color="secondary" size="sm"/>
        <q-icon class="q-mx-sm" name="mdi-youtube" color="secondary" size="sm"/>
      </q-toolbar>
    </q-header>


    <q-page-container class="bg-secondary font-catana">
      <router-view />
    </q-page-container>

  <div class="bg-secondary text-primary q-px-xl q-py-xl font-catana">
    <div class="container row justify-between q-col-gutter-md">
      <!-- Logo et description -->
      <div class="col-12 col-md-3">
        <div class="text-h2 q-mt-xl font-fleur">Diva Mode</div>
        <p class="q-mt-sm">Votre destination mode, alliant élégance et confort.</p>
        
        <div class="row q-gutter-sm q-py-xl text-bold">
          ilyes.amara24@gmail.com <br>
          +33 6 88 67 05 48
        </div>
      </div>
      
      <!-- Liens rapides -->
      <div class="col-12 col-md-3">
        <h6 class="text-h6">Liens rapides</h6>
        <q-list dense>
          <q-item clickable v-ripple to="/shop"><q-item-section>Boutique</q-item-section></q-item>
          <q-item clickable v-ripple to="/about"><q-item-section>À propos</q-item-section></q-item>
          <q-item clickable v-ripple to="/contact"><q-item-section>Contact</q-item-section></q-item>
          <q-item clickable v-ripple to="/faq"><q-item-section>FAQ</q-item-section></q-item>
          <q-item clickable v-ripple to="/faq"><q-item-section>Politique de confidentialité et cookies</q-item-section></q-item>
        </q-list>
      </div>
      
      <!-- Réseaux sociaux -->
      <div class="col-12 col-md-3">
        <h6 class="text-h6">Suivez-nous</h6>
        <div class="row q-gutter-sm">
          <q-btn round flat icon="fab fa-facebook" href="#" target="_blank" />
          <q-btn round flat icon="fab fa-instagram" href="#" target="_blank" />
          <q-btn round flat icon="fab fa-twitter" href="#" target="_blank" />
        </div>
      </div>
    </div>
    
  </div>
  
    <!-- Copyright -->
    <div class=" bg-grey-2 text-center text-grey-6">
      &copy; {{ new Date().getFullYear() }} Mohamed AMARA - Tous droits réservés.
    </div>

  </q-layout>
</template>

<script>

import { ref } from 'vue'

export default {
  setup () {
    return {
      onglet_model: ref('welcome'),

      onglet_options: [
        { label: 'Accueil', value: 'welcome' },
        { label: 'E-boutique', value: 'shop' },
        { label: 'A propos', value: 'about' },
        { label: 'Contact', value: 'contact' }
      ]
    }
  }
}
</script>
