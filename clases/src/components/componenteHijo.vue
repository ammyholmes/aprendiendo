<template>
  <div>
    <p>Datos pasado a traves de propiedad props</p>
    <div v-for="datos in superheroes" :key="datos.nombre">
      <div v-if="datos.activo">
        {{ datos.nombre }}
      </div>
    </div>
    <br />
    <div id="cartas">
      <v-card class="mx-auto" max-width="750">
        <v-toolbar color="indigo" dark>
          <v-toolbar-title>Productos</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>

        <v-container fluid>
          <v-row dense>
            <v-col v-for="card in cards" :key="card.title" :cols="3">
              <v-card>
                <v-img
                    :src="card.src"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="150px"
                >
                  <v-card-title v-text="card.title"></v-card-title>
                </v-img>

                <v-card-text>
                  <h2>
                    {{ card.title }}
                  </h2>
