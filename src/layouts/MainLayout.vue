<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Header / Navbar -->
    <q-header class="navbar" elevated>
      <q-toolbar class="navbar-toolbar">
        <!-- Logo -->
        <q-toolbar-title class="logo">
          <q-icon name="web" color="primary" size="32px" />
          <span>Quasar Fardaus</span>
        </q-toolbar-title>

        <!-- Desktop Menu -->
        <div class="desktop-menu">
          <q-btn flat label="Home" to="/" class="menu-btn" />

          <q-btn flat label="About" class="menu-btn" />

          <q-btn flat label="Services" class="menu-btn" />

          <q-btn flat label="Features" class="menu-btn" />

          <q-btn flat label="Contact" class="menu-btn" />

          <q-btn
            color="primary"
            label="Get Started"
            unelevated
            class="get-started-btn"
          />
        </div>

        <!-- Mobile Menu Button -->
        <q-btn
          flat
          dense
          round
          icon="menu"
          color="primary"
          class="mobile-menu-btn"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <!-- Mobile Drawer -->
    <q-drawer
      v-model="leftDrawerOpen"
      side="right"
      bordered
      overlay
      class="mobile-drawer"
    >
      <q-list padding>
        <q-item-label header class="drawer-title"> Menu </q-item-label>

        <q-item clickable v-close-popup to="/" class="drawer-item">
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>

          <q-item-section> Home </q-item-section>
        </q-item>

        <q-item clickable v-close-popup class="drawer-item">
          <q-item-section avatar>
            <q-icon name="info" />
          </q-item-section>

          <q-item-section> About </q-item-section>
        </q-item>

        <q-item clickable v-close-popup class="drawer-item">
          <q-item-section avatar>
            <q-icon name="design_services" />
          </q-item-section>

          <q-item-section> Services </q-item-section>
        </q-item>

        <q-item clickable v-close-popup class="drawer-item">
          <q-item-section avatar>
            <q-icon name="star" />
          </q-item-section>

          <q-item-section> Features </q-item-section>
        </q-item>

        <q-item clickable v-close-popup class="drawer-item">
          <q-item-section avatar>
            <q-icon name="mail" />
          </q-item-section>

          <q-item-section> Contact </q-item-section>
        </q-item>

        <q-separator class="q-my-md" />

        <q-item>
          <q-item-section>
            <q-btn
              color="primary"
              label="Get Started"
              unelevated
              class="full-width"
            />
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <!-- Page Content -->
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";

const leftDrawerOpen = ref(false);
</script>

<style scoped>
/* Navbar */
.navbar {
  background: white;
  color: #172033;
}

.navbar-toolbar {
  width: 90%;
  max-width: 1200px;
  margin: auto;
  min-height: 75px;
}

/* Logo */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 21px;
  font-weight: 800;
  color: #172033;
}

/* Desktop Menu */
.desktop-menu {
  display: flex;
  align-items: center;
  gap: 5px;
}

.menu-btn {
  color: #475569;
  font-weight: 600;
  padding: 8px 14px;
}

.menu-btn:hover {
  color: #1976d2;
}

.get-started-btn {
  margin-left: 12px;
  border-radius: 8px;
  padding: 0 18px;
}

/* Mobile Menu */
.mobile-menu-btn {
  display: none;
}

/* Drawer */
.mobile-drawer {
  width: 280px;
}

.drawer-title {
  font-size: 20px;
  font-weight: 700;
  color: #172033;
}

.drawer-item {
  border-radius: 8px;
  margin-bottom: 5px;
  color: #475569;
}

.drawer-item:hover {
  background: #eef5ff;
  color: #1976d2;
}

/* Responsive */
@media (max-width: 768px) {
  .navbar-toolbar {
    width: 94%;
  }

  .desktop-menu {
    display: none;
  }

  .mobile-menu-btn {
    display: block;
  }

  .logo {
    font-size: 18px;
  }
}
</style>
