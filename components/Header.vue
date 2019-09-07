<template>
  <div class="head">
    <!-- navbar -->
    <el-menu
      class="nav"
      mode="horizontal"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#fff"
      default-active="1"
      :router="true"
    >
      <el-menu-item index="/">Home</el-menu-item>
      <el-menu-item index="/porto">Works</el-menu-item>
      <el-menu-item style="float:right">
        <a target="_blank" href="https://twitter.com/muh_muflih">Twitter</a>
      </el-menu-item>
      <el-menu-item style="float:right">
        <a target="_blank" href="https://www.linkedin.com/in/muhammad-muflih-574b2b71">Linkedin</a>
      </el-menu-item>
      <el-menu-item style="float:right">
        <a target="_blank" href="https://www.instagram.com/m_muflih5/">Instagram</a>
      </el-menu-item>
      <el-menu-item style="float:right">
        <a target="_blank" href="https://github.com/mmuflih55">Github</a>
      </el-menu-item>
      <el-menu-item v-if="search==true" style="float:right">
        <el-input
          placeholder="Search by post name"
          v-model="searchstr"
          suffix-icon="search"
          class="search"
        />
      </el-menu-item>
    </el-menu>
    <!-- end of navbar -->
    <!-- toggle btn -->
    <div class="togglenav">
      <a class="togglemenu-btn" @click="tglmenu">
        <i class="el-icon-menu"></i>
      </a>
    </div>
    <el-menu
      class="menu-toggle"
      background-color="#545c64"
      text-color="#fff"
      :collapse="isCollapse"
      :router="true"
    >
      <el-menu-item index="/">
        <span slot="title">Home</span>
      </el-menu-item>
      <el-menu-item index="/porto">
        <span slot="title">Works</span>
      </el-menu-item>
      <el-submenu index="3">
        <template slot="title">
          <span slot="title">Social Media</span>
        </template>
        <el-menu-item-group>
          <el-menu-item>
            <a target="_blank" href="https://twitter.com/muh_muflih">Twitter</a>
          </el-menu-item>
          <el-menu-item>
            <a target="_blank" href="https://www.linkedin.com/in/muhammad-muflih-574b2b71">Linkedin</a>
          </el-menu-item>
          <el-menu-item>
            <a target="_blank" href="https://www.instagram.com/m_muflih5/">Instagram</a>
          </el-menu-item>
          <el-menu-item>
            <a target="_blank" href="https://github.com/mmuflih55">Github</a>
          </el-menu-item>
        </el-menu-item-group>
      </el-submenu>
    </el-menu>
    <!-- end of toggle btn -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchstr: "",
      allowsearch: true,
      activeIndex: "1",
      isCollapse: true
    };
  },
  watch: {
    searchstr() {
      if (this.allowsearch == true) {
        setTimeout(() => {
          console.log(this.searchstr);
          this.allowsearch = true;
        }, 1000);
      }
      this.allowsearch = false;
    }
  },
  props: ["search"],
  methods: {
    to(path) {
      this.$router.push(path);
    },
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    tglmenu() {
      this.isCollapse = !this.isCollapse;
    },
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<style scoped>
@media only screen and (max-width: 600px) {
  .nav {
    display: none;
  }

  .head {
    padding-bottom: 7vh;
  }

  .togglenav {
    display: flex;
    align-items: center;
  }
}
@media only screen and (min-width: 600px) {
  .head {
    padding-bottom: 0;
  }

  .nav {
    display: block;
  }

  .togglenav {
    display: none;
  }
  .menu-toggle {
    display: none;
  }
}

.el-menu--collapse {
  top: 7vh;
  width: 0;
  height: 93vh;
}

.el-menu--collapse * {
  display: none;
}

.togglenav {
  background-color: #545c64;
  padding: 10px;
  height: 7vh;
  vertical-align: middle;
  width: 100vw;
  position: fixed;
}
.togglemenu-btn {
  color: white;
  padding: 5px;
  left: 0;
}
.menu-toggle {
  position: fixed;
}
.menu-toggle a {
  text-decoration: none;
}
.menu-toggle a:visited {
  color: white;
}
.menu-toggle:not(.el-menu--collapse) {
  top: 7vh;
  width: 200px;
  min-height: 93vh;
}

.nav a {
  text-decoration: none !important;
}
</style>
