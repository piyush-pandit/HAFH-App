<template>
  <ion-page>
    <ion-content fullscreen>
      <div>
        <div class="ion-padding-bottom">
          <img
            class="main"
            src="http://d2u4q3iydaupsp.cloudfront.net/M9YO50StNO9wcaIKVYLMIAVeaOrWxAHoEXoIO0K1D9hMa6RlXDkuExDgDwGnn1NTP70WO5k6SoYUhqA2jEzvSp5Fj0jmHNjAWq11rOt0OA59j6pLWSEK6jEWMrGxtiG2"
          />
        </div>
        <ion-list class="ion-padding-end">
          <ion-item class="ion-margin-bottom">
            <ion-avatar slot="start">
              <img
                src="https://essblog.wpengine.com/wp-content/uploads/2020/05/rv-renovation-ideas.jpg"
              />
            </ion-avatar>
            <ion-label>
              <h2><strong>Bedroom</strong></h2>
            </ion-label>
          </ion-item>

          <ion-item class="ion-margin-bottom">
            <ion-avatar slot="start">
              <img
                src="https://koa.com/blog/images/2017-Airstream-Flying-Cloud.jpg?preset=blogPhoto"
              />
            </ion-avatar>
            <ion-label>
              <h2><strong>Kitchen</strong></h2>
            </ion-label>
          </ion-item>

          <ion-item class="ion-margin-bottom">
            <ion-avatar slot="start">
              <img
                src="https://kiowacountypress.net/sites/default/files/field/image/cost-effective_rv_maintenance_tips.jpg"
              />
            </ion-avatar>
            <ion-label>
              <h2><strong>Rv Maintanence</strong></h2>
            </ion-label>
          </ion-item>
        </ion-list>
      </div>
      <ion-fab
        @click="openAddRoom()"
        horizontal="end"
        vertical="bottom"
        slot="fixed"
      >
        <ion-fab-button color="primary" style="margin:auto">
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
        <h6>New Area</h6>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonContent,
  IonItem,
  IonAvatar,
  IonLabel,
  IonIcon,
  IonFab,
  IonFabButton,
  modalController,
} from "@ionic/vue";
import { defineComponent } from "vue";
import { add } from "ionicons/icons";
import RoomAddModal from "./RoomAddModal.vue";
export default defineComponent({
  components: {
    IonContent,
    IonItem,
    IonAvatar,
    IonLabel,
    IonIcon,
    IonFab,
    IonFabButton,
  },
  setup() {
    return {
      add,
    };
  },
  methods: {
    async openAddRoom() {
      const modal = await modalController.create({
        component: RoomAddModal,
        cssClass: "my-custom-class",
        swipeToClose: true,
        componentProps: {
          title: "New Title",
        },
      });
      return modal.present();
    },
  },
});
</script>

<style scoped>
ion-icon {
  font-size: 30px;
}

.main {
  border-radius: 0px 0px 20px 20px;
}

/* .list-avatar {
  margin-top: 20px;
  size: 50px;
} */
</style>
