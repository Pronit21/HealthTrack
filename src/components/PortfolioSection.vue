<template>
    <v-container class="my-15 text-center">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4">
                    Centres
                </v-subheader>
                <p>Experience the benefits of regular exercise with gym workouts or soccer sessions to improve your fitness and overall health.</p>

            </v-col>
            <v-col lg="12">
                <div class="text-center">
                    <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp' ? 'success' : ''"
                        class="mx-5">Gyms</v-chip>
                    <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp' ? 'success' : ''"
                        class="mx-5">Yoga Centres</v-chip>

                    <v-chip @click="activePortfolio = 'desktopapp'"
                        :color="activePortfolio === 'desktopapp' ? 'success' : ''" class="mx-5">Sports</v-chip>



                </div>

            </v-col>
            <slot v-if="activePortfolio === 'webapp'">

                <v-col lg="3" v-for="(web, webindex) in webApps" :key="webindex">
                    <v-card>
                        <v-img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8Z3ltfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)" height="200px">
                            <v-card-title>{{ web.title }}
                            </v-card-title>

                        </v-img>
                    </v-card>

                </v-col>
            </slot>

            <slot v-if="activePortfolio === 'mobileapp'">
                <v-col lg="3" v-for="(mobile, mobileindex) in mobileApps" :key="mobileindex">
    <v-card>
        <v-img src="https://images.unsplash.com/photo-1551958219-acbc608c6377?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8c29jY2VyfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="white--text align-end"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)" height="200px">
            <v-card-title>{{ mobile.title }}
            </v-card-title>

        </v-img>
    </v-card>

</v-col>

</slot>

<slot v-if="activePortfolio === 'desktopapp'">

<v-col lg="3" v-for="(desktop, desktopindex) in desktopApps" :key="desktopindex">
    <v-card>
        <v-img src="https://images.unsplash.com/photo-1551958219-acbc608c6377?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8c29jY2VyfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" class="white--text align-end"
            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)" height="200px">
            <v-card-title>{{ desktop.title }}
            </v-card-title>

        </v-img>
    </v-card>

</v-col>
</slot>
            

        </v-row>

    </v-container>
</template>

<script>
export default{
    name: "PortfolioSection",
    data() {
        return {
            activePortfolio: 'webapp',
            webApps: [
                { title: 'Parklane', image: './../assets/gym1.jpg' },
                { title: 'Urban', image: './../assets/gym1.avif' },
                { title: 'Baner', image: './../assets/gym3.avif' },
                { title: 'Lavale', image: './../assets/ai-generated-7866239_960_720.jpg' },
                { title: 'Gateway', image: './../assets/dinosaur.png' },
                
            ],

            mobileApps: [
                { title: 'Yoga Centre 1', image: './../assets/ai-generated-7866239_960_720.jpg' },
                { title: 'Yoga Centre 2', image: './../assets/dinosaur.png' },
                { title: 'Yoga Centre 3', image: './../assets/cafe-7441426_960_720.webp' },
                { title: 'Yoga Centre 4', image: './../assets/drawing-7502248_960_720.jpg' },
               
                

        ],

        desktopApps: [
                { title: 'Sport Clubs 1', image: './../assets/ai-generated-7866239_960_720.jpg' },
                { title: 'Sport Clubs 2', image: './../assets/dinosaur.png' },
                { title: 'Sport Clubs 3', image: './../assets/cafe-7441426_960_720.webp' },
                { title: 'Sport Clubs 4', image: './../assets/drawing-7502248_960_720.jpg' },
                { title: 'Sport Clubs 5', image: './../assets/girl.png' },
                { title: 'Sport Clubs 6', image: './../assets/mushroom.png'}

        ]



           
          
        }
    }
}

</script>

<style scoped>

.text-h4{
    font-weight: bold;
}
</style>