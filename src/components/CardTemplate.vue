<template>
    <div class="center-wrapper">
      <v-row justify="center" align="center" class="card-row" dense>
        <!-- Card 1 -->
        <v-col cols="12" sm="6" md="4">
          <v-card
            class="expandable-card"
            icon @click="toggleShow('card1')"
          >
            <v-img
              src="../assets/Yellow Mecha.png"
            ></v-img>
            <v-card-title>Yellow Mecha</v-card-title>
            <v-card-subtitle>Yellow Mecha robot from Taiwan</v-card-subtitle>
            <br>
            <br>
            <v-expand-transition>
              <div v-show="show.card1" class="expandable-content">
                <v-divider></v-divider>
                <v-card-text>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
                  Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                  Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        <!-- Card 2 -->
        <v-col cols="12" sm="6" md="4">
          <v-card
            class="expandable-card"
            icon @click="toggleShow('card2')"
          >
            <v-img
              src="../assets/A black mecha.png"
            ></v-img>
            <v-card-title>Black Mecha</v-card-title>
            <v-card-subtitle>Black Mecha robot from Japan</v-card-subtitle>
            <br>
            <br>
            <v-expand-transition>
              <div v-show="show.card2" class="expandable-content">
                <v-divider></v-divider>
                <v-card-text>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
                  Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                  Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        <!-- Card 3 -->
        <v-col cols="12" sm="6" md="4">
          <v-card
            class="expandable-card"
            icon @click="toggleShow('card3')"
          >
            <v-img
              src="../assets/A blue mecha.png"
            ></v-img>
            <v-card-title>Blue Mecha</v-card-title>
            <v-card-subtitle>Blue Mecha robot from USA</v-card-subtitle>
            <br>
            <br>
            <v-expand-transition>
              <div v-show="show.card3" class="expandable-content">
                <v-divider></v-divider>
                <v-card-text>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
                  Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                  Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </template>
  
  <script>
  export default {
    data: () => ({
      show: {
        card1: false,
        card2: false,
        card3: false,
      },
    }),
    methods: {
      toggleShow(card) {
        this.show[card] = !this.show[card];
      },
    },
  };
  </script>
  
  <style scoped>
  .center-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #121212; /* Dark background for dark mode */
  }
  
  .card-row {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .expandable-card {
    width: 344px;
    transition: height 0.3s ease-in-out;
    background-color: #1e1e1e; /* Dark card background */
    color: #ffffff; /* White text */
  }
  
  .expandable-content {
  height: 120px; /* Fixed height */
  overflow: hidden; /* Ensure excess text isn't shown */
}

.v-card-text {
  max-height: 120px; /* Controls the height of the text */
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: initial; /* Allows text to wrap */
  display: -webkit-box;
  -webkit-line-clamp: 3; /* Display up to 3 lines of text */
  -webkit-box-orient: vertical; /* Vertical flow for clamped lines */
}
  </style>
  