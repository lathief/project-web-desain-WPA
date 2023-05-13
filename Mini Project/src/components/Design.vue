<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Design</v-subheader>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit</p>
            </v-col>
            <v-col lg="12">
                <div class="text-center">
                    <v-chip @click="activeDesign = 'house'" :color="activeDesign == 'house'?'success':''" class="mx-5">House</v-chip>
                    <v-chip @click="activeDesign = 'hospital'" :color="activeDesign == 'hospital'?'success':''" class="mx-5">Hospital</v-chip>
                    <v-chip @click="activeDesign = 'university'" :color="activeDesign == 'university'?'success':''" class="mx-5">University</v-chip>
                </div>
            </v-col>

            <slot v-if="activeDesign == 'house'">
            <v-col lg="3" v-for="(house,houseindex) in House" :key="houseindex">
                <v-card>
                    <v-img
                        src="house.image"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                    >
                        <v-card-title>{{house.title}}</v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            </slot>
            <slot v-if="activeDesign == 'hospital'">
            <v-col lg="3" v-for="(hospital,hospitalindex) in Hospital" :key="hospitalindex">
                <v-card>
                    <v-img
                        src="hospital.image"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                    >
                        <v-card-title>{{hospital.title}}</v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            </slot>
            <slot v-if="activeDesign == 'university'">
            <v-col lg="3" v-for="(university,universityindex) in University" :key="universityindex">
                <v-card>
                    <v-img
                        src="university.image"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                    >
                        <v-card-title>{{university.title}}</v-card-title>
                    </v-img>
                </v-card>
            </v-col>
            </slot>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name:"Design",
        data(){
            return{
                activeDesign:"house",
                House:[
                    {title:"House Design 1", image:""},
                    {title:"House Design 2", image:""},
                    {title:"House Design 3", image:""},
                    {title:"House Design 4", image:""},
                    {title:"House Design 5", image:""},
                    {title:"House Design 6", image:""},
                    {title:"House Design 7", image:""},
                ],
                Hospital:[
                    {title:"Hospital Design 1", image:""},
                    {title:"Hospital Design 2", image:""},
                    {title:"Hospital Design 3", image:""},
                    {title:"Hospital Design 4", image:""},
                    {title:"Hospital Design 5", image:""},
                ],
                University:[
                    {title:"University Design 1", image:""},
                    {title:"University Design 2", image:""},
                    {title:"University Design 3", image:""},
                    {title:"University Design 4", image:""},
                    {title:"University Design 5", image:""},
                    {title:"University Design 6", image:""},
                ]
            }
        }
    }
</script>
<style scoped>

</style>>