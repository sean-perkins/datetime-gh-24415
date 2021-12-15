<template>
  <ion-item
    id="datepicker"
    button
    detail="false"
  >
    <ion-label>Date example</ion-label>
    <ion-icon
      slot="end"
      :icon="calendarOutline"
    />
    <ion-popover
      trigger="datepicker"
      size="cover"
      show-backdrop="false"
      translucent
    >
      <ion-datetime
        first-day-of-week="1"
        hour-cycle="h23"
        size="cover"
        show-default-time-label="false"
        :presentation="presentation"
      />
    </ion-popover>
</ion-item>
</template>

<script lang="ts">
import { IonPopover, IonDatetime, IonIcon, IonItem, IonLabel } from '@ionic/vue'

export default {
  name: 'ExploreContainer',
  props: {
    name: String
  },
  components: {IonPopover, IonDatetime, IonIcon, IonItem, IonLabel}
}
</script>

<style scoped>
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