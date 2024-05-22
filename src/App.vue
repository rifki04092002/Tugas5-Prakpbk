<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="Menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          ALAT-ALAT GUNUNG
        </q-toolbar-title>

        <q-btn dense flat round icon="Akun" @click="toggleRightDrawer" />
      </q-toolbar>

      <q-tabs align="left"> </q-tabs>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <div class="q-pa-md">
        <q-item-label header>Katagori</q-item-label>
        <q-item to="/tents">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/f5/4b/ad/f54badb091cdc307ce604a225b306784.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Tenda Gunung</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/clothing">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/2e/44/1e/2e441e0a1b493b5d8423bad36c1f8685.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Sepatu Gunung</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/gear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/7b/49/11/7b4911d9b6996c5d9c7e2cb0d8109df1.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Tas Gunung</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/bear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/564x/83/6b/f1/836bf1cb94256a6117a40962fa13b567.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Sleeping Bag</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/bear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/7f/51/ed/7f51ed585cd8988fc02c29d2fd45e897.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Pakaian dan Jaket Gunung</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/bear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/7a/82/cf/7a82cf33a00b28023d35ae38125de54a.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Matras</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/bear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/9d/cc/b6/9dccb6179acb0bf260949779c8e81347.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Perlengkapan Masak</q-item-label>
          </q-item-section>
        </q-item>
        <q-item to="/bear">
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/2c/a6/da/2ca6da753b7085b0570a3d9a5a0d9741.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Headlamp</q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <div class="q-pa-md">
        <q-item-label header>Account</q-item-label>
        <q-item>
          <q-item-section avatar>
            <q-avatar>
              <img
                src="https://i.pinimg.com/474x/3a/fd/26/3afd26d1ae54c115389e3e1b27a63495.jpg"
              />
            </q-avatar>
          </q-item-section>
          <q-item-section>
            <q-item-label>Rifki Nul Arif</q-item-label>
            <q-item-label caption>rifkinularif0409@gmail.com</q-item-label>
          </q-item-section>
        </q-item>
        <q-separator />
        <q-item-label header>Profil</q-item-label>
        <q-item>
          <q-item-section>
            <q-item-label>Nama :</q-item-label>
          </q-item-section>
          <q-item-section side> Rifki Nul Arif </q-item-section>
        </q-item>
        <q-item>
          <q-item-section>
            <q-item-label>Nomor HP :</q-item-label>
          </q-item-section>
          <q-item-section side> 081276349548 </q-item-section>
        </q-item>
        <q-item>
          <q-item-section>
            <q-item-label>Alamat :</q-item-label>
          </q-item-section>
          <q-item-section side> Kuansing </q-item-section>
        </q-item>
        <q-item>
          <q-item-section>
            <q-item-label>Hobi :</q-item-label>
          </q-item-section>
          <q-item-section side> Jelaja Alam </q-item-section>
        </q-item>
      </div>
    </q-drawer>

    <q-layout view="hHh lpR fFf">
      <!-- Header and other elements -->

      <q-page-container>
        <div class="q-pa-md">
          <q-carousel swipeable animated v-model="slide" thumbnails infinite>
            <q-carousel-slide
              :name="1"
              class="carousel-slide"
              img-src="https://i.pinimg.com/474x/ca/a3/a5/caa3a5125e1188790848eedb7951eafb.jpg"
            />
            <q-carousel-slide
              :name="2"
              class="carousel-slide"
              img-src="https://i.pinimg.com/474x/87/9f/54/879f544eac8717b3ae2c87db88022e14.jpg"
            />
            <q-carousel-slide
              :name="3"
              class="carousel-slide"
              img-src="https://i.pinimg.com/474x/18/a0/4e/18a04e478de4881e4d1635c57dd28b0d.jpg"
            />
            <q-carousel-slide
              :name="4"
              class="carousel-slide"
              img-src="https://i.pinimg.com/474x/ce/f4/db/cef4db9c104216e34bc8736d422ab6d7.jpg"
            />
          </q-carousel>
        </div>
      </q-page-container>

      <!-- Footer and other elements -->
    </q-layout>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          <div>GunShop</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const leftDrawerOpen = ref(false);
    const rightDrawerOpen = ref(false);

    return {
      slide: ref(1),
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },

      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
