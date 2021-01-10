<template>
  <v-container fluid fill-height class="About">
    <v-row align-content="center" justify="center" no-gutters>
      <transition appear>
        <v-col cols="12" hight="100px">
          <h3 class="littleTitle">About</h3>
          <h2>自己紹介</h2>
        </v-col>
      </transition>
    </v-row>
    <v-row align-content="center" justify="center" no-gutters>
      <transition appear name="profile">
        <v-col style="height: 50vh" xl="2/3">
          <v-avatar min-height="300" min-width="300">
            <img src="../assets/profile.jpg" alt="myAvatar" class="photo" />
          </v-avatar>
        </v-col>
      </transition>
      <transition appear name="profile">
        <v-col style="height: 50vh" xl="1/3">
          <div class="profile-text">
            <p>仙台市出身。平成11年生まれの大学３年生、高山 伶と申します。</p>
          </div>
        </v-col>
      </transition>
    </v-row>
  </v-container>
</template>

<style lang="scss" scoped>
.About {
  color: rgb(60, 60, 60);
  text-align: center;
  font-size: 32px;
  font-weight: bold;
}

.littleTitle {
  color: rgb(116, 166, 76);
  font-size: 20px;
}

.photo {
  width: 200px;
  height: 200px;
}

.profile-text {
  font-size: 20px;
  text-align: center;
}

.v-enter-active {
  transition: opacity 2s;
}

.v-enter {
  opacity: 0;
}
.v-enter-to {
  opacity: 1;
}

.profile-enter-active {
  transition: opacity 5s;
}

.profile-enter {
  opacity: 0;
}

.profile-enter-to {
  opacity: 1;
}
</style>
