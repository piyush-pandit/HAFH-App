<template>
  <ion-page>
    <ion-content>
      <ion-toolbar>
        <ion-title class="ion-text-center ion-padding">
          <h3>
            Login
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
              <ion-label position="floating">Email </ion-label>
              <ion-input
                type="email"
                placeholder="Enter your Email"
                value=""
              ></ion-input>
            </ion-item>

            <ion-item class="ion-margin-bottom">
              <ion-label position="floating">Password </ion-label>
              <ion-input
                type="password"
                value=""
                placeholder="Enter your password"
              ></ion-input>
            </ion-item>

            <ion-button
              href="/rv"
              expand="block"
              shape="round"
              color="primary"
              fill="solid"
              class="ion-margin-bottom"
              >Sign In</ion-button
            >
            <!-- <a href="/">Forgot Password ?</a> -->

            <p class="ion-padding-top">
              Dont have an account?
              <a href="/signup">
                <ion-text color="primary">Signup here !</ion-text></a
              >
            </p>
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

<style scoped></style>
