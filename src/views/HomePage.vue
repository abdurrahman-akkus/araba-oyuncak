<template>
  <ion-page>

    <ion-content>
      <div class="background-image">
        <div id="container">
          <div style="display: flex;">
            <button class="btn" @click="playSound('start3')">Çalıştır</button>
            <button class="btn" @click="playSound('kapi1')">Kapı</button>
            <button class="btn" @click="playSound('gec')">Bas Gaza</button>
            <button class="btn" @click="playSound('skid1')">Ani Fren</button>
            <button class="btn" @click="playSound('fren')">Fren</button>
            <button class="btn" @click="playSound('el_freni')">El Freni</button>
          </div>
        </div>
        <div style="display: flex;">
          <button class="btn" @click="playSound('hadi_gidelim')">Hadi Gidelim</button>
          <button class="btn" @click="playSound('kirmizi')">Kırmızı</button>
          <button class="btn" @click="playSound('sari')">Sarı</button>
          <button class="btn" @click="playSound('yesil')">Yeşil</button>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script>
import { IonPage } from '@ionic/vue';
export default {
  methods: {
    playSound(sound) {
      const audio = new Audio('/sound/' + sound + '.mp3'); // Sesi yükleyin
      audio.play(); // Sesi çalın
    }
  }
}
</script>

<style scoped>
.background-image {
  background-size: cover;
  background-position: center center;
  background-image: url('/public/img/direksiyon.jpg');
  height: 100vh;
}

.btn {
  width: 9rem;
  height: 6rem;
  margin: 1rem;
  border-radius: 1rem;
  background: #038574;
}

#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
