<template>
  <div class="App max-w-4xl mx-auto px-10">
    <header class="Header w-viewport p-10">
      <saber-link to="/">
        <img src="/logo.svg" />
      </saber-link>
      <div class="Navbar">
        <slot name="header">
          <saber-link to="/cv">CV</saber-link>
          <saber-link to="/projects">Projects</saber-link>
        </slot>
      </div>
    </header>
    <main class="Body">
      <slot></slot>
    </main>
    <footer class="Footer w-viewport p-10 flex remove-margin">
      <slot name="footer">
        <p class="gray">Limitless Loop &copy; 2019</p>
        <saber-link to="/about" class="w-content">About</saber-link>
      </slot>
    </footer>
  </div>
</template>

<style scoped>
.Header {
  display: flex;
}
.Navbar {
  flex-grow: 1;
  display: flex;
  justify-content: flex-end;
}
.Navbar a {
  margin-left: 20px;
  line-height: 32px;
}

.w-content {
  flex-grow: 0;
}
</style>