<template>
  <ion-page>
    <!-- <ion-header :translucent="true"> </ion-header> -->
    <ion-toolbar class="ion-no-border">
      <ion-item class="ion-no-padding ion-no-border">
        <ion-avatar slot="end">
          <img
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ492AnNAAPJR3tuNh9iojWzyaVnyeQ3mApIw&usqp=CAU"
          />
        </ion-avatar>
      </ion-item>
    </ion-toolbar>
    <ion-content class="ion-padding">
      <ion-toolbar>
        <ion-title>
          <h3 class="title">Your Rv's</h3>
        </ion-title>
      </ion-toolbar>

      <ion-list class="ion-padding-top">
        <ion-item class="ion-no-padding ion-margin-bottom" href="/room">
          <ion-avatar slot="start">
            <img
              src="https://st.depositphotos.com/1203257/1763/i/950/depositphotos_17637335-stock-photo-yellowstone-rv-trip.jpg"
            />
          </ion-avatar>

          <ion-label>Radnor Family Rv</ion-label>
          <ion-badge color="primary" class="ion-margin-end">10+</ion-badge>
          <div>
            <div class="circle">
              <ion-text color="light">
                <ion-icon src="/assets/icon/share.svg"></ion-icon>
              </ion-text>
            </div>
            <div class="small">
              Share
            </div>
          </div>
        </ion-item>
        <ion-item class="ion-no-padding ion-margin-bottom" href="/room">
          <ion-avatar slot="start">
            <img
              src="https://st.depositphotos.com/1203257/1763/i/950/depositphotos_17637335-stock-photo-yellowstone-rv-trip.jpg"
            />
          </ion-avatar>

          <ion-label>Radnor Family Rv</ion-label>
          <ion-badge color="primary" class="ion-margin-end">10+</ion-badge>
          <div>
            <div color="primary" class="circle">
              <ion-text color="light">
                <ion-icon src="/assets/icon/share.svg"></ion-icon>
              </ion-text>
            </div>
            <div class="small">
              Share
            </div>
          </div>
        </ion-item>
      </ion-list>
      <ion-fab
        style="margin-bottom:60px"
        @click="openAddRv"
        horizontal="end"
        vertical="bottom"
        slot="fixed"
      >
        <ion-fab-button color="primary" style="margin:auto">
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
        <h6>Add an RV</h6>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonPage,
  IonTitle,
  IonToolbar,
  IonHeader,
  IonContent,
  IonIcon,
  IonAvatar,
  IonButton,
  IonModal,
  IonBadge,
  IonFab,
  IonFabButton,
  modalController,
} from "@ionic/vue";
import { add } from "ionicons/icons";
import RvAddModal from "./RvAddModal.vue";
export default {
  name: "Rv",
  component: {
    IonPage,
    IonToolbar,
    IonTitle,
    IonHeader,
    IonContent,
    IonIcon,
    IonAvatar,
    IonButton,
    IonModal,
    IonBadge,
    IonFab,
    IonFabButton,
  },
  setup() {
    return {
      add,
    };
  },
  methods: {
    async openAddRv() {
      const modal = await modalController.create({
        component: RvAddModal,
        cssClass: "my-custom-class",
        swipeToClose: true,
        componentProps: {
          title: "New Title",
        },
      });
      return modal.present();
    },
  },
};
</script>

<style scoped>
.circle {
  width: 22px;
  height: 22px;
  background: #ffab01;
  font-size: 12px;
  border-radius: 50%;
  padding: 4px;
  margin: 0 auto;
}
.small {
  font-size: 12px;
}
</style>
