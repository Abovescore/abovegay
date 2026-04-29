<script setup lang="ts">
//
</script>

<template>
  <div class="container">
    <div class="box">
      <p class="box-title">my sona.</p>
      <div class="box-content">
        <div class="sona-header">
          <img src="/sona/cosmi.webp" alt="Cosmi" class="sona-ref" />
          <div class="sona-details">
            <h1>Cosmi</h1>
            <ul class="traits">
              <li><span class="label">Body Type</span>Anthro</li>
              <li><span class="label">Pronouns</span>he/him</li>
              <li><span class="label">Gender</span>Male</li>
              <li><span class="label">Species</span>Cat</li>
            </ul>
          </div>
        </div>
        <p class="bio">
          Cosmi is a skinny black cat that usually wears a vibrant-purple thin T-Shirt that only covers one shoulder. His hair covers his eyes, and the inside of his ears are purple. Usually followed by a large, purple butterfly (their name is Pueblo)
        </p>
      </div>
    </div>

    <div class="rules-row">
      <div class="box do-box">
        <p class="box-title">do!</p>
        <div class="box-content">
          <ul class="rules-list">
            <li>Permissionless art</li>
            <li>Design alterations</li>
            <li>Human/demihuman versions</li>
            <li>SFW art</li>
          </ul>
        </div>
      </div>
      <div class="box dont-box">
        <p class="box-title">don't...</p>
        <div class="box-content">
          <ul class="rules-list">
            <li>NSFW art</li>
            <li>Fetish art</li>
            <li>Gore art</li>
            <li>AI "art"</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="art-grid">
      <div class="box cosmi-art">
        <a href="/sona/dreamalgia.png" target="_blank" class="art-link">
          <img src="/sona/dreamalgia.png" alt="Commission from Dreamalgia" loading="lazy"/>
        </a>
        <div class="art-info">
          <p class="artist">Commission from <a href="https://xcancel.com/dreamalgia">Dreamalgia</a></p>
          <p class="description">It's so peak,,,</p>
        </div>
      </div>
      <div class="box cosmi-art">
        <a href="/sona/firstart.png" target="_blank" class="art-link">
          <img src="/sona/firstart.png" alt="First drawing" loading="lazy"/>
        </a>
        <div class="art-info">
          <p class="artist">Gift from an IRL friend</p>
          <p class="description">First drawing of him</p>
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

.sona-header {
  display: flex;
  gap: 20px;
  align-items: flex-start;
}

.sona-ref {
  width: 200px;
  border-radius: 8px;
  object-fit: cover;
}

.sona-details h1 {
  margin: 0 0 12px;
  font-size: 28px;
  font-weight: 700;
  color: #fff;
}

.traits {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-size: 15px;
}

.label {
  color: rgb(150 114 255 / 0.8);
  font-weight: 600;
  margin-right: 8px;
}

.label::after {
  content: ':';
}

.bio {
  margin: 16px 0 0;
  font-size: 15px;
  line-height: 1.7;
  color: rgb(200 190 220 / 0.85);
}

.rules-row {
  display: flex;
  gap: 12px;
}

.rules-row .box {
  flex: 1;
}

.rules-list {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 6px;
  font-size: 14px;
  color: rgb(200 190 220 / 0.85);
}

.rules-list li::before {
  content: '•';
  color: #9b6dff;
  margin-right: 8px;
}

.art-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.cosmi-art {
  width: calc(50% - 6px);
  box-sizing: border-box;
}

.art-link {
  display: block;
  aspect-ratio: 1;
  overflow: hidden;
}

.cosmi-art img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.3s;
}

.cosmi-art:hover img {
  transform: scale(1.03);
}

.art-info {
  padding: 10px;
}

.artist {
  margin: 0 0 2px;
  color: rgb(150 114 255 / 0.8);
}

.artist a {
  color: #9b6dff;
  text-decoration: none;
  transition: color 0.2s;
}

.artist a:hover {
  color: #b99aff;
  text-decoration: underline;
}

.description {
  margin: 0;
  font-size: 13px;
  color: rgb(200 190 220 / 0.6);
}
</style>
