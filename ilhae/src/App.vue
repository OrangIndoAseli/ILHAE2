<script setup lang="ts">
import { ref } from 'vue'

const isDark = ref(false)
const toggleTheme = () => {
  isDark.value = !isDark.value
  if(isDark.value) {
    document.documentElement.setAttribute('data-theme', 'dark')
  } else {
    document.documentElement.removeAttribute('data-theme')
  }
}
</script>

<template>
  <div class="app-wrapper">
    <!-- Navbar -->
    <nav class="navbar container">
      <div class="nav-inner neu-flat">
        <a href="#" class="logo-nav">ILHAE</a>
        <div class="nav-links">
          <a href="#pengenalan">Pengenalan</a>
          <a href="#struktur">Struktur</a>
          <a href="#proyek">Proyek</a>
          <a href="#bergabung">Daftar</a>
        </div>
        <div class="nav-actions">
          <button @click="toggleTheme" class="theme-btn" aria-label="Toggle Theme">
            <svg v-if="!isDark" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>
            <svg v-else width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="5"></circle><line x1="12" y1="1" x2="12" y2="3"></line><line x1="12" y1="21" x2="12" y2="23"></line><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line><line x1="1" y1="12" x2="3" y2="12"></line><line x1="21" y1="12" x2="23" y2="12"></line><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line></svg>
          </button>
        </div>
      </div>
    </nav>

    <!-- Bagian 1: Pengenalan -->
    <section id="pengenalan" class="container hero-wrapper">
      <div class="hero-text">
        <p class="hero-tag">UKM Informatika</p>
        <h1>Welcome to <span>ILHAE</span></h1>
        <p class="hero-desc">
          Informatics Laboratory Hub for Achievement & Excellent. Komunitas mahasiswa Informatika yang berfokus pada kolaborasi, inovasi, dan prestasi di dunia nyata.
        </p>
        <a href="#bergabung" class="neu-btn">Bergabung Sekarang →</a>
      </div>
      <div class="hero-image">
        <div class="hero-logo-bg neu-circle">
          <img src="/image/logo-ilhae.png" alt="ILHAE Logo" />
        </div>
      </div>
    </section>

    <!-- Bagian 2: Struktur -->
    <section id="struktur" class="container">
      <h2 class="section-title">Struktur Organisasi</h2>

      <div class="org-tree">
        <!-- Tier 1: Full-Stack -->
        <div class="org-tier tier-1">
          <div class="org-node neu-flat">
            <div class="member-avatar neu-circle">
              <img src="/image/rio.jpeg" alt="Rio" />
            </div>
            <span class="role-badge">FULL-STACK DEVELOPER</span>
          </div>
        </div>

        <!-- Connector line top -->
        <div class="connector-down"></div>
        <div class="connector-horizontal tier2-line"></div>

        <!-- Tier 2: FE + BE -->
        <div class="org-tier tier-2">
          <div class="org-node-group">
            <div class="connector-up-left"></div>
            <div class="org-node neu-flat">
              <div class="members-row">
                <div class="member-avatar neu-circle"><img src="/image/siti.jpeg" alt="Siti" /></div>
                <div class="member-avatar neu-circle"><img src="/image/yandra.jpeg" alt="Yandra" /></div>
              </div>
              <span class="role-badge">FRONT-END DEVELOPER</span>
            </div>
          </div>

          <div class="org-node-group">
            <div class="connector-up-right"></div>
            <div class="org-node neu-flat">
              <div class="members-row">
                <div class="member-avatar neu-circle"><img src="/image/hadi.jpeg" alt="Hadi" /></div>
                <div class="member-avatar neu-circle"><img src="/image/wana.jpg" alt="Wana" /></div>
                <div class="member-avatar neu-circle"><img src="/image/fajar.jpeg" alt="Fajar" /></div>
              </div>
              <span class="role-badge">BACK-END DEVELOPER</span>
            </div>
          </div>
        </div>

        <!-- Connector line middle -->
        <div class="connector-horizontal tier3-line"></div>

        <!-- Tier 3: UI/UX + ML -->
        <div class="org-tier tier-2">
          <div class="org-node-group">
            <div class="connector-up-left"></div>
            <div class="org-node neu-flat">
              <div class="members-row">
                <div class="member-avatar neu-circle"><img src="/image/anggi.jpeg" alt="Anggi" /></div>
              </div>
              <span class="role-badge">UI/UX DESIGN</span>
            </div>
          </div>

          <div class="org-node-group">
            <div class="connector-up-right"></div>
            <div class="org-node neu-flat">
              <div class="members-row">
                <div class="member-avatar neu-circle"><img src="/image/rehan.jpeg" alt="Rehan" /></div>
                <div class="member-avatar neu-circle"><img src="/image/fatur.jpeg" alt="Fatur" /></div>
              </div>
              <span class="role-badge">MACHINE LEARNING / DL</span>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- Bagian 3: Proyek Lomba -->
    <section id="proyek" class="container">
      <h2 class="section-title">Proyek & Lomba</h2>

      <!-- Aplikasi Web -->
      <div class="project-category">
        <div class="cat-label neu-inset">Aplikasi Web</div>
        <div class="projects-grid">
          <div class="project-card neu-flat">
            <div class="proj-img-wrap neu-inset">
              <img class="web-img" src="/image/tanibijak.jpeg" alt="TaniBijak" />
            </div>
            <div class="project-info">
              <h3>Hackathon IYREF - SRE ITB</h3>
              <span class="proj-badge">Semifinal / 4th</span>
            </div>
          </div>
          <div class="project-card neu-flat">
            <div class="proj-img-wrap neu-inset">
              <img class="web-img" src="/image/lingkunganku.jpeg" alt="Lingkunganku" />
            </div>
            <div class="project-info">
              <h3>Lingkunganku</h3>
              <span class="proj-badge">Dalam Proses Seleksi</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Aplikasi Mobile -->
      <div class="project-category">
        <div class="cat-label neu-inset">Aplikasi Mobile</div>
        <div class="projects-grid mobile-grid">
          <div class="project-card neu-flat">
            <div class="proj-img-wrap neu-inset">
              <img class="mobile-img" src="/image/jekman.jpg" alt="Jekman" />
            </div>
            <div class="project-info">
              <h3>Jekman - GEMASTIK XIX</h3>
              <span class="proj-badge">Dalam Proses Seleksi</span>
            </div>
          </div>
          <div class="project-card neu-flat">
            <div class="proj-img-wrap neu-inset">
              <img class="mobile-img" src="/image/svara.jpeg" alt="Svara" />
            </div>
            <div class="project-info">
              <h3>SVARA - GEMASTIK XIX</h3>
              <span class="proj-badge">Dalam Proses Seleksi</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Bagian 4: Daftar -->
    <section id="bergabung" class="container">
      <div class="join-banner neu-inset">
        <div class="join-content">
          <h2>Tertarik Bergabung?</h2>
          <p>Jadilah bagian dari komunitas kami. Belajar, berkarya, dan berprestasi bersama ILHAE!</p>
          <a href="https://wa.me/6281910519479" target="_blank" rel="noopener noreferrer" class="neu-btn">
            Daftar via WhatsApp
          </a>
        </div>
        <div class="join-logo">
          <div class="neu-circle" style="width:200px;height:200px;display:flex;justify-content:center;align-items:center;">
            <img src="/image/logo-ilhae.png" alt="ILHAE" style="width:70%;"/>
          </div>
        </div>
      </div>
    </section>

    <footer class="footer-bar">
      <p>&copy; 2026 ILHAE — Informatics Laboratory Hub for Achievement & Excellent</p>
    </footer>
  </div>
</template>
