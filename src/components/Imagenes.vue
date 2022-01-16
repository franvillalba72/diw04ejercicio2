<template>
    <div id="imagenes">
        <div class="thumbnail">
            <a @click="ponerImagen(1)"><img v-bind:src="imagen[1]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/></a>
            <a @click="ponerImagen(2)"><img v-bind:src="imagen[2]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/></a>
            <a @click="ponerImagen(3)"><img v-bind:src="imagen[3]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/></a>
            <a @click="ponerImagen(4)"><img v-bind:src="imagen[4]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/></a>
            <a @click="ponerImagen(5)"><img v-bind:src="imagen[5]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/></a>
        </div>
        <div class="imagen-mostrar">
            <img v-bind:src="imagen[0]" alt="E-Bike Trekking Biwbik LANS" copyright="cc-by BiwBik"/>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Imagenes',
  data() {
    return {
      imagen: [
        require('../assets/lans-600x600.jpg'),
        require('../assets/lans-600x600.jpg'),
        require('../assets/lans2-600x600.jpg'),
        require('../assets/lans3-600x600.jpg'),
        require('../assets/lans11-600x600.jpg'),
        require('../assets/lans16-600x600.jpg'),
      ],
    };
  },
  methods: {
    ponerImagen(id) {
      this.imagen[0] = this.imagen[id];
    },
  },
};
</script>

<style>
    #imagenes {
        display: flex;
        border-radius: 25px;
        padding: 1em;
        margin: 1em;
    }
    .imagen-mostrar {
        flex-grow: grow;
        width: 600px;
        height: 600px;
        margin-right: 5em;
    }
    .thumbnail {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }
    .thumbnail img {
        width: 100px;
        border: 1px solid;
        margin-bottom: 1.5em;
    }
</style>
