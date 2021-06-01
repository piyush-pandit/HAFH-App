<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-button @click="closeRoomAddModal()">
            <ion-icon :icon="arrowBack"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Add Room/Area</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <div class="ion-padding-vertical input-universal">
        <ion-label>Name Of Room/Area</ion-label>
        <ion-input placeholder="Enter your Room" class="bg-custom"></ion-input>
      </div>

      <div class="ion-padding-vertical input-universal">
        <ion-label>Add an Image</ion-label>
        <ion-input placeholder="Add an Image" class="bg-custom"></ion-input>
      </div>
      <div class="ion-text-center ion-padding-vertical">
        <ion-button
          @click="closeRoomAddModal()"
          color="primary"
          shape="round"
          size="medium"
        >
          Add Room
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
    closeRoomAddModal() {
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
