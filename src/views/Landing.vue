<template>
  <ion-page>
    <!-- <ion-header translucent> -->
    <!-- <ion-toolbar>
        <ion-title>Card</ion-title>
      </ion-toolbar> -->
    <!-- </ion-header> -->
    <ion-content fullscreen>
      <ion-card class="main ion-no-padding ion-no-margin">
        <img
          class="img"
          src="https://imagebee.org/vehicles/motorhome/motorhome-3-1600x1060.jpg"
        />
      </ion-card>
      <ion-card-header class="ion-text-center">
        <ion-card-title>
          <h1>Home <ion-text color="primary">Away From</ion-text> Home</h1>
        </ion-card-title>
      </ion-card-header>
      <div class="ion-text-center">
        <ion-card-content>
          <ion-grid>
            <div class="ui-buttons">
              <ion-row>
                <ion-col class="ion-padding-top" size="6">
                  <div>
                    <ion-button
                      class="ui-button-toggle"
                      @click="toggle"
                      :class="[showSignUp ? 'active' : '']"
                      href="/signup"
                      color="warning"
                      shape="round"
                      fill="solid"
                    >
                      <ion-text color="light">
                        Sign Up
                      </ion-text>
                    </ion-button>
                  </div>
                </ion-col>
                <ion-col class="ion-padding-top" size="6">
                  <div>
                    <ion-button
                      class="ui-button-toggle"
                      @click="toggle"
                      :class="[!showSignUp ? 'active' : '']"
                      color="warning"
                      href="/login"
                      shape="round"
                      fill="outline"
                      >Login</ion-button
                    >
                  </div>
                </ion-col>
              </ion-row>
            </div>
          </ion-grid>
          <ion-row>
            <ion-col class="ion-margin-top">
              <ion-button class="googleBtn" href="" shape="round" color="light"
                ><ion-icon
                  slot="start"
                  src="/assets/icon/google-icon.svg"
                  color="primary"
                ></ion-icon
                >Login with Google</ion-button
              >
            </ion-col>
          </ion-row>
        </ion-card-content>
      </div>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonPage,
  IonCard,
  IonCardContent,
  IonCardTitle,
  IonButton,
  IonIcon,
  IonGrid,
  IonRow,
  IonCol,
} from "@ionic/vue";

import { defineComponent } from "vue";
import { logoGoogle } from "ionicons/icons";

export default defineComponent({
  name: "Home",
  components: {
    IonPage,
    IonCard,
    IonCardContent,
    IonButton,
    IonCardTitle,
    IonIcon,
    IonGrid,
    IonRow,
    IonCol,
  },
  setup() {
    return {
      logoGoogle,
    };
  },
  data() {
    return {
      showSignUp: true,
    };
  },
  methods: {
    toggle() {
      this.showSignUp = !this.showSignUp;
    },
  },
});
</script>

<style scoped>
/* .ion-padding {
  padding-top: 10px;
}
<<<<<<< head .ion-margin-top {
  margin-top: 30px;
}
.main {
  border-radius: 0px 0px 30px 30px;
}
======= .ion-margin-top {
  margin-top: 30px;
}

.main {
  border-radius: 0px 0px 30px 30px;
}

>>>>>>>921fa16873431d8c8757462c71063aee7b7003b7 .googleBtn {
  box-shadow: 0 17px 10px -10px rgba(0, 0, 0, 0.4);
  cursor: pointer;
  transition: all ease-in-out 300ms;
  text-transform: uppercase;
}

.img {
  max-width: 100%;
} */
</style>
