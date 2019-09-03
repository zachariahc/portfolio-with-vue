
<template>
  <v-app light>
    <v-toolbar>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <a href="http://www.github.com/zachariahc" class="top-git-icon">
        <v-icon class="ml-3" size="30" @mouseover="mouseIn" @mouseleave="mouseOut">mdi-github-circle</v-icon>
      </a>
      <p v-show="test" class="mt-5 git-side-text ml-2">Click to check out some of my projects!</p>
    </v-toolbar>
    <v-content>
      <section>
        <v-parallax src="./assets/smoke.jpeg" height="600">
          <v-layout column align-center justify-center class="white--text">
            <v-avatar size="200" color="white">
              <img src="./assets/zachavatar.jpg" alt="avatar" />
            </v-avatar>
            <h1 class="white--text mb-2 display-1 text-center">Zachariah Crowell</h1>
            <div class="subheading mb-4 text-center">Let's build something</div>
            <!-- save button to fire lambda form submit -->
            <v-btn class="mt-12" color="blue lighten-2" dark large @click="dialog= true">Contact</v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-layout column wrap class="my-12" align-center>
          <v-flex xs12 sm4 class="my-4">
            <div class="text-center">
              <h2
                class="headline"
              >"The more I study, the more insatiable do I feel my genius for it to be."</h2>
              <span class="subheading">- Ada Lovelace</span>
            </div>
          </v-flex>
        </v-layout>
        <v-layout class="my-12" justify-space-around wrap>
          <v-flex xs6 md2>
            <v-card flat class="transparent">
              <v-card-text class="text-center">
                <v-icon x-large class="blue--text text--lighten-2">mdi-palette</v-icon>
              </v-card-text>
              <v-card-title primary-title class="layout justify-center">
                <div class="headline text-center">UX/UI Design</div>
              </v-card-title>
              <v-card-text>
                Always comfortable learning something new. Familiar with adobe
                <b>XD</b> and
                <b>photoshop</b> for mock ups and file editing. Currently using
                <b>vuetify</b>, have also worked at length
                with
                <b>bootstrap</b>,
                <b>material design</b>,
                <b>ant</b> and
                <b>bulma</b>.
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs6 md2>
            <v-card flat class="transparent">
              <v-card-text class="text-center">
                <v-icon x-large class="blue--text text--lighten-2">mdi-wrench</v-icon>
              </v-card-text>
              <v-card-title primary-title class="layout justify-center">
                <div class="headline text-center">Tools/Methods</div>
              </v-card-title>
              <v-card-text>
                Well versed in the practices of
                <b>git</b> and
                <b>github</b>. Used to movements on the ticket board using
                <b>jira</b> and well acquainted with the
                <b>agile</b> software development environment.
                <b>Scrums</b>,
                <b>sprints</b> and
                <b>kanban</b> boards a part of my daily routine.
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs6 md2>
            <v-card flat class="transparent">
              <v-card-text class="text-center">
                <v-icon x-large class="blue--text text--lighten-2">mdi-flash</v-icon>
              </v-card-text>
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">Languages</div>
              </v-card-title>
              <v-card-text>
                Primarily a front end developer focused on
                <b>javascript</b> I'm open to new challenges.
                <b>Python</b> has been a focus of free time alongside
                <b>java</b> and
                <b>typescript</b>.
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs6 md2>
            <v-card flat class="transparent">
              <v-card-text class="text-center">
                <v-icon x-large class="blue--text text--lighten-2">mdi-apps</v-icon>
              </v-card-text>
              <v-card-title primary-title class="layout justify-center">
                <div class="headline text-center">Frameworks</div>
              </v-card-title>
              <v-card-text>
                Currently working on a full-time development project using
                <b>vue</b>. I'm experienced with
                <b>react</b>,
                <b>node</b> and use
                <b>serverless</b> framework for deployments to
                <b>GCP</b> and
                <b>AWS</b>
              </v-card-text>
            </v-card>
          </v-flex>
        </v-layout>

        <v-layout justify-space-around wrap style="text-align: center">
          <v-flex xs6 md2 pa-2>
            <img src="./assets/logo-cloud.png" style="height: 35px;" />
          </v-flex>
          <v-flex xs6 md2 pa-2>
            <img src="./assets/reactlogo.png" style="height: 40px;" />
          </v-flex>
          <v-flex xs6 md2 pa-2>
            <img src="./assets/vuelogo.png" style="height: 40px;" />
          </v-flex>
          <v-flex xs6 md2 pa-2>
            <img src="./assets/aws_logo.png" style="height: 40px;" />
          </v-flex>
        </v-layout>
      </section>
      <section>
        <v-parallax src="./assets/bottomsmoke.jpeg" :height="paralaxHeight">
          <h2 class="text-center headline mt-5">Examples Of Work</h2>

          <v-layout align-center justify-space-around row fill-height class="mt-5" text-center wrap>
            <v-flex xs12 md3>
              <a href="https://tesla-mockup.firebaseapp.com/" target="_blank">
                <img src="./assets/tesla-mockup.png" style="height: 225px;" />
              </a>
            </v-flex>
            <v-flex xs12 md3>
              <a href="https://transit-41e17.firebaseapp.com/" target="_blank">
                <img src="./assets/transit-bandit.png" style="height: 225px;" />
              </a>
            </v-flex>
            <v-flex xs12 md3>
              <a
                href="https://github.com/zachariahc/firebase-function-twilio/blob/master/functions/index.js"
                target="_blank"
              >
                <img src="./assets/twilio-thumbnail.png" style="height: 225px;" />
              </a>
            </v-flex>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center>
            <v-flex xs12 sm4>
              <v-card flat class="transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">About</div>
                </v-card-title>
                <v-card-text>
                  Beginner to intermediate level web developer.
                  Open to new opportunities big or small. Looking primamrily
                  for full time long term work. Open to long term contracts as well!
                  <br />
                  <br />
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card flat class="transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Contact</div>
                </v-card-title>
                <v-card-text>I'd love to hear from you! Please reach out with any questions or comments.</v-card-text>
                <v-list class="transparent">
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">mdi-phone</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>720-352-8912</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">mdi-map-marker</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>Denver, CO</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">mdi-email</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>zachariahcrowell@gmail.com</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="blue--text text--lighten-2">mdi-github-circle</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>
                        <a
                          id="git-link"
                          href="https://www.github.com/zachariahc"
                          target="_blank"
                        >github portfolio</a>
                      </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>
      <!-- Footer ready to be used -->
      <v-footer>
        <v-layout row wrap align-center>
          <v-flex xs12></v-flex>
        </v-layout>
      </v-footer>
    </v-content>
    <!-- CONTACT FORM -->

    <v-row justify="center">
      <v-dialog v-model="dialog" persistent max-width="600px">
        <v-card>
          <v-card-title>
            <span class="headline">Contact Form</span>
          </v-card-title>
          <v-card-text>
            <v-container>

              <v-form 
              ref="form"
              v-model="valid"
              >
              <v-row>
                <v-col cols="12" sm="12" md="4">
                  <v-text-field 
                  label="Name*" 
                  :rules="nameRules"
                  v-model="form.name"
                  ></v-text-field>
                </v-col>
                <v-col cols="12" sm="12" md="4">
                  <v-text-field 
                  label="Email*"
                  :rules="emailRules" 
                  v-model="form.reply_to"
                  ></v-text-field>
                </v-col>

                <v-col cols="12">
                  <v-text-field 
                  label="Message*" 
                  :rules="messageRules"
                  v-model="form.message"></v-text-field>
                </v-col>
              </v-row>
              </v-form>

            </v-container>
            <small>*indicates required field</small>
          </v-card-text>
          <v-card-actions>
            <div class="flex-grow-1"></div>
            <v-btn color="blue darken-1" text @click="dialog = false">Close</v-btn>
            <v-btn color="blue darken-1" :disabled="!valid" text @click="getFormData">Send</v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
   <!-- Snackbar confirmation message -->
    <v-snackbar
      v-model="snackbar"
      :timeout="timeout"
    >
      {{ snackBarText }}
      <v-btn
        color="blue"
        text
        @click="snackbar = false"
      >
        Close
      </v-btn>
    </v-snackbar>
  </v-app>
</template>

<script>
import axios from "axios";
export default {
  name: "App",
  components: {},
  data() {
    return {
      title: "Z/C",
      test: false,
      dialog: false,
      sendButton: false,
      valid: true,
      snackbar: false,
      snackBarText: "Thanks. I'll be in touch shortly!",
      timeout: 3000,
      form: {
        name: "",
        reply_to: "",
        message: ""
      },
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 15) || 'Name must be less than 15 characters',
      ],
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      messageRules: [
        v => !!v || 'Please include a message',
        v => (v && v.length <= 500) || 'Please limit message to 500 characters.',
      ],
    };
  },
  computed: {
    paralaxHeight: function() {
      const paralaxControl = this.$vuetify.breakpoint.smAndDown ? 1000 : 400;
      return paralaxControl;
    }
  },
  methods: {
    validate () {
      if (this.$refs.form.validate()) {
          this.snackbar = true
        }
      },
    mouseIn() {
      this.test = true;
    },
    mouseOut() {
      this.test = false;
    },
    getFormData() {
      const formData = this.form;
      try {
        axios.post(
          "https://dwxt1f2tse.execute-api.us-east-1.amazonaws.com/dev/static-site-mailer",
          formData
        );
      } catch (e) {
        console.error(e);
      }
      this.dialog = false;
      this.snackbar = true;
    }
  }
};
</script>

<style>
.top-git-icon {
  text-decoration: none;
}
.top-git-icon:hover {
  opacity: 0.5;
}
.git-side-text {
  color: rgb(75, 74, 74);
}
#git-link {
  text-decoration: none;
  color: black;
}
#git-link:hover {
  text-decoration: none;
  color: rgb(59, 59, 59);
}
</style>