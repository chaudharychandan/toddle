<template>
  <v-toolbar class="elevation-1 px-2" color="white">
    <v-layout row align-center justify-space-between>
      <v-flex xs6 sm1>
        <router-link to="/dashboard">
          <v-layout row class="dashboard-link">
            <v-icon small color="grey">dashboard</v-icon>
            <span class="ml-3">Dashboard</span>
          </v-layout>
        </router-link>
      </v-flex>
      <v-flex xs6 sm2 offset-sm1 class="text-xs-center">
        <router-link to="/">
          <h1 class="grey--text">logo</h1>
        </router-link>
      </v-flex>
      <v-flex sm2 class="hidden-sm-and-down">
        <v-layout row justify-content-end>
          <v-flex>
            <v-avatar class="user-avatar" size="40">
              <img
                src="https://cdn.vuetifyjs.com/images/john.jpg"
                alt="John"
              >
              <span class="green online"></span>
            </v-avatar>
          </v-flex>
          <v-flex>
            <v-btn icon class="ml-5 notifications">
              <v-icon color="grey">notifications</v-icon>
              <span class="green new"></span>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn icon class="ml-5">
              <v-icon color="grey" medium>sort</v-icon>
            </v-btn>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-toolbar>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped lang="scss">
  $default-color: #9e9e9e;
  $active-color: #2196F3;
  $active-bc-color: #E1F5FE;
  .dashboard-link {
    width: 120px;
    padding: 5px;
    border-radius: 2px;
  }
  h1 {
    font-weight: 900;
    font-size: 28px;
  }
  a {
    color: $default-color;
  }
  .router-link-exact-active {
    .dashboard-link{
      background-color: $active-bc-color;
      i, span {
        color: $active-color !important;
      }
    }
  }
  .user-avatar {
    position: relative;
    .online {
      position: absolute;
      height: 14px;
      width: 14px;
      border-radius: 50%;
      bottom: 0px;
      right: 0px;
      border: 2px solid #fff !important;
    }
  }
  .notifications {
    position: relative;
    i {
      -ms-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
      transform: rotate(-20deg);
    }
    .new {
      position: absolute;
      height: 8px;
      width: 8px;
      border: 1px solid #fff !important;
      border-radius: 50%;
      top: 8px;
      right: 12px;
    }
  }
</style>
