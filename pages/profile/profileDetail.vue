<template>
    <div>
        <div class="v-tab-div mt-6">
            <v-tabs background-color="transparent" color="orange">
                <v-tab>BADGES</v-tab>
                <v-tab>STUDYING</v-tab>
                <v-tab>COLLECTION</v-tab>
            </v-tabs>
        </div>
        <div class="d-flex flex-wrap">
            
            <v-card
                class="mt-8 mr-5"
                width="45%"
                outlined
            >
                <v-list-item three-line>
                <v-list-item-avatar
                    size="80"
                ><img src="@/assets/trophy.png" /></v-list-item-avatar>
                <v-list-item-content>
                    <div class="">
                    First Step
                    </div>
                    <v-list-item-subtitle>Pass your first quiz</v-list-item-subtitle>
                </v-list-item-content>
                
                </v-list-item>

            </v-card>

            <v-card
                class="mt-8 mr-5"
                width="45%"
                outlined
            >
                <v-list-item three-line>
                <v-list-item-avatar

                    size="80"
                ><img src="@/assets/certificate.png" /></v-list-item-avatar>
                <v-list-item-content>
                    <div class="">
                    Certificate Unlocked
                    </div>
                    <div>
                    </div>
                    <v-list-item-subtitle>Confirm your name on your certificates</v-list-item-subtitle>
                </v-list-item-content>
                
                </v-list-item>

            </v-card>
            <v-card
                class="mt-8 mr-5"
                width="45%"
                outlined
            >
                <v-list-item three-line>
                <v-list-item-avatar
                    size="80"
                ><img src="@/assets/book.png" /></v-list-item-avatar>
                <v-list-item-content>
                    <div class="">
                    Book Worm
                    </div>
                    <v-list-item-subtitle>Complete all of the practice course lessons</v-list-item-subtitle>
                </v-list-item-content>
                
                </v-list-item>

            </v-card>
            <v-card
                class="mt-8 mr-5"
                width="45%"
                outlined
            >
                <v-list-item three-line>
                <v-list-item-avatar
                    size="80"
                ><img src="@/assets/program.jpg" /></v-list-item-avatar>
                <v-list-item-content>
                    <div class="">
                    Training Wheels
                    </div>
                    <v-list-item-subtitle>Complete the portal tutorial</v-list-item-subtitle>
                </v-list-item-content>
                
                </v-list-item>

            </v-card>
            
            
            <v-card
                class="mt-8 mr-5"
                width="45%"
                outlined
            >
                <v-list-item three-line>
                <v-list-item-avatar
                    size="80"
                ><img src="@/assets/exam.png" /></v-list-item-avatar>
                <v-list-item-content>
                    <div class="">
                    Final Exam
                    </div>
                    <v-list-item-subtitle>Pass the practice course final exam</v-list-item-subtitle>
                </v-list-item-content>
                
                </v-list-item>

            </v-card>
        </div>
    </div>
</template>