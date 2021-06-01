<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-button @click="closePostAddModal()">
            <ion-icon :icon="arrowBack"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Add Post</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <div class="ion-padding-vertical input-universal">
        <ion-label>Add a Status</ion-label>
        <ion-input placeholder="Add a Status" class="bg-custom"></ion-input>
      </div>

      <div class="ion-padding-vertical input-universal">
        <ion-label>Add an Image</ion-label>
        <ion-input placeholder="Add an Image" class="bg-custom"></ion-input>
      </div>
      <div class="ion-text-center  ion-padding-vertical">
        <ion-button
          @click="closePostAddModal()"
          color="primary"
          shape="round"
          size="medium"
        >
          Post This
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
    closePostAddModal() {
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
