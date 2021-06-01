<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-button @click="closeRvAddModal()">
            <ion-icon :icon="arrowBack"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Add an Rv</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <div class="ion-padding-vertical input-universal">
        <ion-label>Name Of Rv</ion-label>
        <ion-input placeholder="Family Rv" class="bg-custom"></ion-input>
      </div>

      <div class="ion-padding-vertical input-universal">
        <ion-label>Add an Image</ion-label>
        <ion-input placeholder="Add an Image" class="bg-custom"></ion-input>
      </div>
      <div class="ion-text-center ion-padding-vertical">
        <ion-button shape="round" fill="outline" color="primary" size="medium">
          <ion-icon
            src="/assets/icon/share.svg"
            class="ion-padding-end"
          ></ion-icon>

          Share With People
        </ion-button>
      </div>
      <div class="ion-text-center">
        <ion-button
          @click="closeRvAddModal()"
          color="primary"
          shape="round"
          size="medium"
        >
          Add Rv
        </ion-button>
      </div>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonPage,
  IonContent,
  IonIcon,
  IonButton,
  modalController,
} from "@ionic/vue";
import { arrowBack } from "ionicons/icons";
export default {
  name: "RvModal",
  components: {
    IonPage,
    IonContent,
    IonIcon,
    IonButton,
  },
  setup() {
    return { arrowBack };
  },
  methods: {
    closeRvAddModal() {
      modalController.dismiss();
    },
  },
};
</script>

<style>
.bg-custom {
  background: #f1f1f1;
}
.input-universal ion-input {
  margin-top: 5px;
}
</style>
