<template>
  <ion-page>
    <ion-content>
      <ion-toolbar>
        <ion-title class="ion-text-center ion-padding">
          <h3>
            Register
          </h3>
        </ion-title>
      </ion-toolbar>
      <ion-card>
        <ion-card-content class="ion-padding-top">
          <ion-card-title class="ion-text-center ion-padding-top">
            <h1>Home <ion-text color="primary">Away From</ion-text> Home</h1>
          </ion-card-title>
          <ion-list>
            <ion-item>
              <ion-label position="floating">Username </ion-label>
              <ion-input
                type="text"
                placeholder="Enter your username"
                value=""
              ></ion-input>
            </ion-item>
            <ion-item>
              <ion-label position="floating">Email</ion-label>
              <ion-input
                type="email"
                placeholder="Enter your Email"
                value=""
              ></ion-input>
            </ion-item>
            <ion-item>
              <ion-label position="floating">Password </ion-label>
              <ion-input
                type="password"
                value=""
                placeholder="Enter your password"
              ></ion-input>
            </ion-item>
            <ion-item class="ion-margin-bottom">
              <ion-label position="floating">Confirm Password</ion-label>
              <ion-input
                type="password"
                value=""
                placeholder="Confirm your password"
              ></ion-input>
            </ion-item>
            <ion-button
              href="/rv"
              expand="block"
              shape="round"
              color="primary"
              fill="solid"
            >
              Sign Up
            </ion-button>
          </ion-list>
        </ion-card-content>
      </ion-card>
    </ion-content>
  </ion-page>
</template>

<script>
import {
  IonContent,
  IonPage,
  IonToolbar,
  IonTitle,
  IonItem,
  IonLabel,
  IonInput,
  IonButton,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  components: {
    IonContent,
    IonPage,
    IonToolbar,
    IonTitle,
    IonItem,
    IonLabel,
    IonInput,
    IonButton,
  },
  setup() {
    return {};
  },
});
</script>

<style scoped>
/* ion-input {
  font-size: 0.9rem;
  --padding-start: 36px;
  --padding-top: 36px;
  color: #7b7b7b;
}

ion-label {
  position: absolute;
  margin-left: 35px;
  font-weight: bold;
  font-size: 0.8rem;
  top: 3px;
} */
/* ion-content {
    
    --background: url("/assets/icon/loginBackground.jpg") no-repeat center/cover fixed ;
} */

/* ion-content {
  position: absolute;
  top: 30%;
  left: 0%;
  right: 50%;
  margin: 0 auto;
  margin-top: 0;
  margin-left: 0;
} */
</style>
