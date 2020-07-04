<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="10">
        <v-row class="main_contents">
          <v-col
            sm="4"
            md="4"
            lg="4"
            xl="4"
            cols="12"
            class="d-flex flex-column justify-start align-center"
          >
            <v-img
              :src="require('~/assets/icon_image.png')"
              height="125"
              max-height="125"
              width="125"
              max-width="125"
            ></v-img>
            <h3 class="mt-6">Taro Tanaka</h3>
            <v-btn dark class="mt-4" @click="dialog = true">Edit</v-btn>
          </v-col>

          <v-col sm="8" md="8" lg="8" xl="8" cols="12">
            <div>
              <h3>Special Skill</h3>
              <p>
                特技は特にありません。
              </p>
            </div>
            <div class="mt-6">
              <h3>Hobby</h3>
              <ul>
                <li>Dead by Daylight</li>
                <li>寝ること</li>
                <li>走ること</li>
              </ul>
            </div>
            <div class="mt-6">
              <h3>Likes and Dislikes</h3>
              <P>食べ物に好き嫌いはありません。</P>
            </div>
            <div class="mt-6">
              <h3>Comment</h3>
              <p>よろしくお願いします</p>
            </div>
          </v-col>
        </v-row>
      </v-col>
      <v-dialog v-model="dialog" persistent max-width="450">
        <v-card>
          <v-card-title class="headline">Edit Your Profile</v-card-title>
          <v-card-text>
            <v-form ref="form" lazy-validation>
              <v-text-field
                v-model="skill"
                :counter="100"
                label="Special Skill"
                required
              ></v-text-field>
              <v-text-field
                v-model="hobby[0]"
                label="Hobby1"
                required
              ></v-text-field>
              <v-text-field
                v-model="hobby[1]"
                label="Hobby2"
                required
              ></v-text-field>
              <v-text-field
                v-model="hobby[2]"
                label="Hobby3"
                required
              ></v-text-field>
              <v-text-field
                v-model="like"
                label="like"
                :counter="100"
                required
              ></v-text-field>
            </v-form>
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn color="red darken-1" text @click="cancelProfile">
              Cancel
            </v-btn>
            <v-btn color="green darken-1" text @click="saveProfile">
              Save
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  components: {},
  data() {
    return { dialog: false, skill: '', hobby: ['', '', ''], like: '' }
  },
  methods: {
    cancelProfile() {
      this.skill = ''
      this.hobby = ['', '', '']
      this.like = ''
      this.dialog = false
    },
    saveProfile() {
      this.dialog = false
    },
  },
}
</script>

<style>
.main_contents {
  border: solid;
  border-color: gray;
}
</style>
