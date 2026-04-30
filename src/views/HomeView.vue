<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";
import dayjs from "dayjs";

const startDate = dayjs("2011-05-18");
const yearsSince = ref("0.000000000");

function updateDate() {
  const now = dayjs();
  yearsSince.value = now.diff(startDate, "year", true).toFixed(9);
}
let interval: any;

onMounted(() => {
  updateDate();
  interval = setInterval(updateDate, 50);
});

onUnmounted(() => {
  clearInterval(interval);
});
</script>

<template>
  <div class="container">
    <div class="box">
      <p class="box-title">about.</p>
      <div class="box-content">
        <h1>heyo, i'm above.</h1>
        <p>
          I'm a <span class="mono age">{{ yearsSince }}</span> y/o self-taught fullstack developer
          from the United States.<br />
          You probably know me for making web prохіеs. I dislike working in a team, usually making
          solo projects. I also build Geometry Dash levels, and enjoy self-hosting.<br />
          I use CachyOS (btw) as my primary operating system, and also enjoy 3D printing (extrusion
          & resin).<br />
          I am a furry too. You can find info and art of my sona
          <RouterLink to="/cosmi">here.</RouterLink><br />
          This site is in Vue + TS, and is also hosted on
          <a href="https://above.nekoweb.org">Nekoweb.</a>
        </p>
      </div>
    </div>

    <div class="box">
      <p class="box-title">my tools.</p>
      <div class="box-content">
        <section>
          <h2>IDEs</h2>
          <div class="tool-pill">
            <icon-simple-icons-jetbrains class="tool-icon" />
            <p>Anything JetBrains</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-zedindustries class="tool-icon" />
            <p>Zed</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-vscodium class="tool-icon" />
            <p>VSCodium</p>
          </div>
        </section>

        <section>
          <h2>Languages</h2>
          <div class="tool-pill">
            <icon-simple-icons-typescript class="tool-icon" />
            <p>TypeScript</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-javascript class="tool-icon" />
            <p>JavaScript</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-python class="tool-icon" />
            <p>Python</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-luau class="tool-icon" />
            <p>Luau</p>
          </div>
          <div class="tool-pill">
            <icon-lucide-coffee class="tool-icon" />
            <p>Java</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-gnubash class="tool-icon" />
            <p>GNU Bash</p>
          </div>
        </section>

        <section>
          <h2>UI</h2>
          <div class="tool-pill">
            <icon-simple-icons-vuedotjs class="tool-icon" />
            <p>Vue.js</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-vite class="tool-icon" />
            <p>Vike</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-radixui class="tool-icon" />
            <p>Radix Primitives</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-react class="tool-icon" />
            <p>React</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-nextdotjs class="tool-icon" />
            <p>Next.js</p>
          </div>
        </section>

        <section>
          <h2>Other</h2>
          <div class="tool-pill">
            <icon-simple-icons-cachyos class="tool-icon" />
            <p>Linux</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-express class="tool-icon" />
            <p>Express</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-cloudflare class="tool-icon" />
            <p>Cloudflare</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-sqlite class="tool-icon" />
            <p>SQLite</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-docker class="tool-icon" />
            <p>Docker</p>
          </div>
          <div class="tool-pill">
            <icon-simple-icons-redis class="tool-icon" />
            <p>Redis</p>
          </div>
        </section>
      </div>
    </div>

    <div class="webring-container">
      <div class="webring-controls">
        <a href="https://silly.city/prev?user=above">
          <icon-lucide-arrow-left class="webring-arrow" />
        </a>
        <a href="https://silly.city/">
          <img src="/gif/sillycitywebring.gif" alt="Silly City" class="webring-icon" />
        </a>
        <a href="https://silly.city/next?user=above">
          <icon-lucide-arrow-right class="webring-arrow" />
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 32px;
  padding: 40px 0;
  color: #e0daf0;
}

.box {
  border: 1px solid rgb(150 114 255 / 0.15);
  border-radius: 5px;
  overflow: hidden;
}

.box-title {
  margin: 0;
  padding: 10px;
  font-size: 14px;
  font-weight: 600;
  color: rgb(150 114 255 / 0.7);
  border-bottom: 1px solid rgb(150 114 255 / 0.1);
}

.box-content {
  padding: 15px;
}

.box-content h1 {
  margin: 0 0 12px;
  font-size: 28px;
  font-weight: 700;
  color: #fff;
}

.box-content h2 {
  font-size: 16px;
  font-weight: 600;
  color: rgb(150 114 255 / 0.8);
}

.box-content h2:first-child {
  margin-top: 0;
}

.box-content p {
  margin: 0;
  line-height: 1.7;
  font-size: 15px;
  color: rgb(200 190 220 / 0.85);
}

.box-content a {
  color: #9b6dff;
  text-decoration: none;
  transition: color 0.2s;
}

.box-content a:hover {
  color: #b99aff;
  text-decoration: underline;
}

.age {
  font-variant-numeric: tabular-nums;
  color: #b99aff;
}

section {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  align-items: center;
  margin-bottom: 16px;
}

section:last-child {
  margin-bottom: 0;
}

section h2 {
  width: 100%;
  margin-bottom: 0;
}

.tool-pill {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 6px 14px;
  border-radius: 8px;
  border: 1px solid rgb(150 114 255 / 0.15);
  background: rgb(150 114 255 / 0.06);
  transition:
    border-color 0.2s,
    background 0.2s;
}

.tool-pill:hover {
  border-color: rgb(150 114 255 / 0.35);
  background: rgb(150 114 255 / 0.1);
}

.tool-pill p {
  margin: 0;
  font-size: 14px;
  color: #d0c8e8;
}

.tool-icon {
  font-size: 18px;
  color: #9b6dff;
}

.webring-container {
  display: flex;
  justify-content: center;
  margin-top: 32px;
}

.webring-controls {
  display: flex;
  align-items: center;
  gap: 12px;
}

.webring-arrow {
  font-size: 24px;
  color: #9b6dff;
  transition: color 0.2s;
}

.webring-arrow:hover {
  color: #b99aff;
}

.webring-icon {
  width: 60px;
  height: auto;
  image-rendering: pixelated;
}
</style>
