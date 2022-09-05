<template>
    <v-footer dark padless>
        <v-col lg="12">
            <v-row justify="center">
                <v-col lg="4" class="text-center">
                    <v-toolbar-title>House Builder</v-toolbar-title>
                          <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-subheader>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam harum eveniet doloribus enim beatae expedita error perspiciatis quia unde itaque corrupti nihil fugiat, facilis labore sed sequi asperiores, modi in.
      </v-subheader>
      <v-form class="mt-4">
        <v-text-field label="Email" outlined dense/>
        <v-btn rounded color="success">Subscribe</v-btn>
      </v-form>
      <div class="mt-10">
        <v-divider></v-divider>
        <v-subheader>Copyright House Builder. All Rights Reserved {{ new Date().getFullYear() }}
                <v-spacer/>
        <strong>Designed by Latif</strong></v-subheader>

      </div>
                </v-col>
            </v-row>
        </v-col>
  </v-footer>
</template>

<script>
    export default{
        name: "Footer",
        data(){
            return{
                      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
            }
        }
    }
</script>

<style scoped>

</style>