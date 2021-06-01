<template>
  <ion-Page>
    <ion-content>
      <ion-card>
        <img
          class="img"
          src="https://cdn.motor1.com/images/mgl/Yozrw/s1/queensize-camper-inside-two-van.jpg"
        />
        <ion-card-title style="margin: 10px 25px 10px"
          ><strong>Your List</strong></ion-card-title
        >
        <ion-item>
          <ion-avatar slot="start">
            <img
              src="https://miro.medium.com/max/600/1*PiHoomzwh9Plr9_GA26JcA.png"
            />
          </ion-avatar>
          <ion-label>
            <h3>Chintan Shah</h3>
            <p>20/05/2021</p>
          </ion-label>
          <ion-button
            class="btn"
            color="primary"
            size="small"
            href="/"
            shape="round"
            fill="outline"
            >Add to Old</ion-button
          >
        </ion-item>
        <img
          class="post-img"
          src="https://learn.compactappliance.com/wp-content/uploads/2017/12/steamed-broccoli.jpg"
        />
        <span style="margin: 25px">Buy Broccoli</span><br /><br />
        <p class="line"><span>Old</span></p>

        <ion-item>
          <ion-avatar slot="start">
            <img
              src="https://miro.medium.com/max/600/1*PiHoomzwh9Plr9_GA26JcA.png"
            />
          </ion-avatar>
          <ion-label>
            <h3>Chintan shah</h3>
            <p>20/05/2021</p>
          </ion-label>
        </ion-item>
        <div class="container">
          <img
            class="post-img"
            src="http://images2.fanpop.com/images/photos/5400000/Random-Food-random-5409310-1280-800.jpg"
          />
        </div>
      </ion-card>
      <ion-fab horizontal="end" vertical="bottom" slot="fixed">
        <ion-fab-button
          @click="openAddPost()"
          color="primary"
          style="margin:auto"
        >
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
        New Post
      </ion-fab>
    </ion-content>
  </ion-Page>
</template>

<script>
import {
  IonCard,
  IonItem,
  IonAvatar,
  IonLabel,
  IonButton,
  IonIcon,
  IonFab,
  IonFabButton,
  modalController,
} from "@ionic/vue";
import { defineComponent } from "vue";
import { add } from "ionicons/icons";
import PostAddModal from "./PostAddModal.vue";
export default defineComponent({
  components: {
    IonCard,
    IonItem,
    IonAvatar,
    IonLabel,
    IonButton,
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
    async openAddPost() {
      const modal = await modalController.create({
        component: PostAddModal,
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
.img {
  border-radius: 0px 0px 30px 30px;
}

.line {
  width: 100%;
  text-align: center;
  border-bottom: 1px solid #abb7b7;
  line-height: 0.1em;
  margin: 10px 0 20px;
}

.line span {
  background: #fff;
  padding: 0 10px;
}

.post-img {
  border-radius: 20px;
  padding-left: 10px;
  padding-right: 10px;
}

.btn {
  float: right;
}

.container {
  position: relative;
}

.top-right {
  position: absolute;
  top: 3px;
  right: 10px;
  font-size: 15px;
  color: rgb(102, 96, 96);
}
</style>
