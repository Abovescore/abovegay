<script setup lang="ts">
//
</script>
<template>
  <div class="container">
    <div class="box">
      <p class="box-title">contact.</p>
      <div class="box-content">
        <p class="subtitle">Feel free to reach out through any of these.</p>
        <div class="contact-list">

          <a href="https://discord.com/users/820451041752776754" target="_blank" rel="noopener noreferrer" class="contact-item">
            <icon-simple-icons-discord class="contact-icon" />
            <div class="contact-info">
              <span class="contact-label">Discord</span>
              <span class="contact-value">@ab.ve</span>
            </div>
            <icon-lucide-external-link class="contact-arrow" />
          </a>

          <a href="mailto:contact@above.gay" class="contact-item">
            <icon-lucide-mail class="contact-icon" />
            <div class="contact-info">
              <span class="contact-label">Email</span>
              <span class="contact-value">contact@above.gay</span>
            </div>
            <icon-lucide-external-link class="contact-arrow" />
          </a>

          <a href="https://github.com/Abovescore" target="_blank" rel="noopener noreferrer" class="contact-item">
            <icon-simple-icons-github class="contact-icon" />
            <div class="contact-info">
              <span class="contact-label">GitHub</span>
              <span class="contact-value">Abovescore</span>
            </div>
            <icon-lucide-external-link class="contact-arrow" />
          </a>

          <a href="https://x.com/above_score" target="_blank" rel="noopener noreferrer" class="contact-item">
            <icon-simple-icons-twitter class="contact-icon" />
            <div class="contact-info">
              <span class="contact-label">Twitter</span>
              <span class="contact-value">@above_score</span>
            </div>
            <icon-lucide-external-link class="contact-arrow" />
          </a>

          <a href="https://gdbrowser.com/u/Abovescore" target="_blank" rel="noopener noreferrer" class="contact-item">
            <icon-simple-icons-geode class="contact-icon" />
            <div class="contact-info">
              <span class="contact-label">Geometry Dash</span>
              <span class="contact-value">Abovescore</span>
            </div>
            <icon-lucide-external-link class="contact-arrow" />
          </a>

        </div>
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

.subtitle {
  margin: 0 0 16px;
  font-size: 14px;
  color: rgb(200 190 220 / 0.7);
}

.contact-list {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 12px 16px;
  border: 1px solid rgb(150 114 255 / 0.15);
  border-radius: 8px;
  text-decoration: none;
  transition: border-color 0.2s, background 0.2s;
}

.contact-item:hover {
  border-color: rgb(150 114 255 / 0.35);
  background: rgb(150 114 255 / 0.06);
}

.contact-icon {
  font-size: 22px;
  color: #9b6dff;
  flex-shrink: 0;
}

.contact-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.contact-label {
  font-size: 14px;
  font-weight: 600;
  color: #fff;
}

.contact-value {
  font-size: 13px;
  color: rgb(200 190 220 / 0.7);
}

.contact-arrow {
  font-size: 16px;
  color: rgb(150 114 255 / 0.4);
  flex-shrink: 0;
  transition: color 0.2s;
}

.contact-item:hover .contact-arrow {
  color: #9b6dff;
}
</style>
