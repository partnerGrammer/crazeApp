<template>
  
        <ion-tabs>
            <ion-tab tab="profile">
                
            </ion-tab>
            <ion-tab tab="closet">
                
            </ion-tab>
            <ion-tab tab="history">
                
            </ion-tab>
            <ion-tab tab="sidebar">
                
            </ion-tab>

            <!-- Use v-slot:bottom with Vue ^2.6.0 -->
            <template slot="bottom">
                <ion-tab-bar>
                    <ion-tab-button tab="profile" to="/profile">
                        <ion-icon name="calendar"></ion-icon>
                        <ion-label>Profile</ion-label>
                    </ion-tab-button>

                    <!-- Provide a custom route to navigate to -->
                    <ion-tab-button tab="closet" to="/closet">
                        <ion-icon name="contacts"></ion-icon>
                        <ion-label>Closet</ion-label>
                    </ion-tab-button>

                    <!-- Provide extra data to route -->
                    <ion-tab-button tab="history" to="/history">
                        <ion-icon name="map"></ion-icon>
                        <ion-label>History</ion-label>
                    </ion-tab-button>

                    <!-- Provide custom click handler -->
                    <ion-tab-button tab="sidebar" to="/">
                        <ion-icon name="information-circle"></ion-icon>
                        <ion-label>Menu</ion-label>
                    </ion-tab-button>
                </ion-tab-bar>
            </template>
        </ion-tabs>
   
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style>

</style>