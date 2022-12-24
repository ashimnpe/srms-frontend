<template>
  <navbar
    position="fixed"
    type="edxplor"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
    class="navbar"
  >
    <template>
      <router-link v-popover:popover1 class="navbar-brand" to="/">
        SHANKER DEV CAMPUS
      </router-link>
      <!-- <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Designed by Invision. Coded by Creative Tim
        </div>
      </el-popover> -->
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
        <nav-link to="/about" class=" text-white nav-link">
          <i class="now-ui-icons users_circle-08"></i> About us
        </nav-link>
      </li>
      <li class="nav-item">
        <nav-link to="/programs" class=" text-white nav-link">
          <i class="now-ui-icons users_circle-08"></i> Programs
        </nav-link>
      </li>
      <li class="nav-item">
        <nav-link to="/contact" class=" text-white nav-link">
          <i class="now-ui-icons users_circle-08"></i> Contact
        </nav-link>
      </li>
      <li class="nav-item">
        <nav-link to="/login" class=" text-white nav-link">
          <i class="now-ui-icons users_circle-08"></i> Login
        </nav-link>
      </li>
    </template>
  </navbar>
</template>

<script>
import { DropDown, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    Navbar,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped>

</style>
