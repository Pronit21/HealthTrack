<template>
    <v-container class="my-15 text-center">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4" justify="center">
                    Healthy Meals
                </v-subheader>
                <p>Order nutritious and delicious meals to fuel your body and mind!</p>

            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                   

                    <v-img height="250"  src="./../assets/grilled-chicken-breast-baked-sweet-potato-boiled-broccoli-black-plate-dark-concrete-background_268847-734.avif"></v-img>

                    <v-card-title>Grilled Chicken Breast with Sweet Potato and Broccoli</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.7 (410)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $11
                        </div>

                        <div> Chicken breast, sweet potato, broccoli, olive oil, salt, pepper, garlic powder
                        </div>
                    </v-card-text>

                   
                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                   

                    <v-img height="250" src="./../assets/Roasted-Veggie-and-Crispy-Chickpea-Salad-7.jpg"></v-img>

                    <v-card-title>Quinoa Salad with Roasted Vegetables and Chickpeas</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.6 (513)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $12
                        </div>

                        <div>Quinoa, bell peppers, zucchini, eggplant, chickpeas, olive oil, lemon juice, salt, pepper, cumin
                        </div>
                    </v-card-text>

                    <v-divider class="mx-4"></v-divider>

                    

                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                    

                    <v-img height="250" src="./../assets/Baked-Salmon-Steak-with-Herbs-and-Lemons-800x530.png"></v-img>

                    <v-card-title>Baked Salmon with Brown Rice and Asparagus</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.9 (473)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $10
                        </div>

                        <div>Salmon fillet, brown rice, asparagus, olive oil, lemon juice, garlic, salt, pepper
                        </div>
                    </v-card-text>

                    <v-divider class="mx-4"></v-divider>

                   

                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                    

                    <v-img height="250" src="./../assets/Ground-Turkey-Chili-1.jpg"></v-img>

                    <v-card-title>Turkey chili</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.8 (523)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $16
                        </div>

                        <div>Ground turkey, black beans, kidney beans, diced tomatoes, onion, garlic, chili powder, cumin, salt, pepper
                        </div>
                    </v-card-text>

                    <v-divider class="mx-4"></v-divider>

                    

                    

                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                   

                    <v-img height="250" src="./../assets/loaded-sweet-potato-5.jpg"></v-img>

                    <v-card-title>Baked sweet potato with black beans and salsa</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.8 (523)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $8
                        </div>

                        <div>Sweet potato, black beans, salsa, avocado, cilantro
                        </div>
                    </v-card-text>

                    <v-divider class="mx-4"></v-divider>

                    

                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
            <v-col>
                <v-card :loading="loading" class="mx-auto my-12" max-width="365">
                    

                    <v-img height="250" src="./../assets/Lentil Soup.jpg"></v-img>

                    <v-card-title>Lentil soup with vegetables
</v-card-title>

                    <v-card-text>
                        <v-row align="center" class="mx-0">
                            <v-rating :value="4.5" color="amber" dense half-increments readonly size="14"></v-rating>

                            <div class="grey--text ms-4">
                                4.7 (510)
                            </div>
                        </v-row>

                        <div class="my-4 text-subtitle-1">
                            $12
                        </div>

                        <div> lentils, carrots, celery, onion, garlic, vegetable broth, tomato paste, cumin, coriander
                        </div>
                    </v-card-text>

                    <v-divider class="mx-4"></v-divider>

                   
                    <v-card-actions>
                        <v-btn color="deep-purple lighten-2" text @click="reserve">
                            Order
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: "ProjectSection"
}


</script>

<style scoped>
.text-h4{
    font-weight: bold;
}

</style>