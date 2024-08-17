<script setup>
import SearchContacs from './components/SearchContacs.vue';
import ListContacs from './components/ListContacs.vue';
//
import { getAllContacts } from './Services/apiContacs'
const title = "Mi Agenda -Lista de Contactos";
const listContacts = getAllContacts()
</script>

<template>
  <div class="flex items-center flex-col p-5">
    <h1 class="text-xl m-4">{{ title }}</h1>
    <SearchContacs/>
    <ListContacs title="Lista de Resultados"
    :listContacts="listContacts"/>
   
  </div>
</template>

<style scoped></style>
