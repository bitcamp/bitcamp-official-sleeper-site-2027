<template>
  <div class="header-container">
    <div class="logo">
      <img
        class="logo-ring"
        src="../assets/img/images/logo-star-ring.svg"
        alt=""
        aria-hidden="true"
      />
      <span class="logo-text">bitcamp</span>
    </div>
    <div class="header-content">
      <h1 class="header-title">
        We're out exploring but we'll see you in April 2027!
      </h1>
      <div class="socials">
        <p>Follow our socials for updates!</p>
        <SocialIcons />
      </div>
      <div class="header-body">
        <LinkButton
          text="I'm Interested!"
          link="https://forms.gle/SmhTejVeN65okvZL6"
        />
        <!-- <LinkButton text="Register Now!" link="https://register.bit.camp/" /> -->
        <!-- uncomment when organizer applications open -->
        <!-- <LinkButton
          text="Become an Organizer!"
          link="https://bit.camp/orgapp"
        /> -->
        <!-- <LinkButton text="Sponsor Us!" link="https://bit.camp/sponsor" /> -->
      </div>
    </div>
    <a
      id="mlh-trust-badge"
      style="
        display: block;
        max-width: 100px;
        min-width: 60px;
        position: fixed;
        right: 50px;
        top: 0;
        width: 10%;
        z-index: 10000;
      "
      href="https://mlh.io/na?utm_source=na-hackathon&utm_medium=TrustBadge&utm_campaign=2026-season&utm_content=white"
      target="_blank"
      ><img
        src="https://logged-assets.s3.amazonaws.com/trust-badge/2027/mlh-trust-badge-2027-white.svg"
        alt="Major League Hacking 2026 Hackathon Season"
        style="width: 100%"
      />
    </a>

    <div class="graphics">
      <img class="trees" src="../assets/img/images/new-trees.svg" alt="trees" />
      <img
        class="trees-small"
        src="../assets/img/images/trees-small.svg"
        alt="trees"
      />
      <img
        class="campfire"
        src="../assets/img/images/campfire.svg"
        alt="campfire"
      />
    </div>
  </div>
</template>

<script lang="ts">
import LinkButton from "~/components/LinkButton.vue";
import SocialIcons from "~/components/SocialIcons.vue";
export default {
  name: "AppHeader",
  components: { LinkButton, SocialIcons },
};
</script>

<style scoped>
.header-container {
  position: relative;
  display: flex;
  align-items: center;
  flex-direction: column;
  padding-bottom: 30vw;
  margin-bottom: 15vw;
  padding-top: 75px;
  gap: 2.8vw;
  text-align: center;
  background: linear-gradient(
    180deg,
    hsla(227, 42%, 13%, 1),
    hsla(234, 27%, 31%, 1)
  );
}

.logo {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: min(420px, 78vw);
  z-index: 5;
}

.logo-ring {
  position: absolute;
  width: 100%;
  transform: rotate(-25.66deg);
  pointer-events: none;
  z-index: 0;
}

.logo-text {
  position: relative;
  z-index: 1;
  font-family: Aleo;
  font-weight: 700;
  font-size: 4.2rem;
  color: white;
}

.header-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2.6vw;
  font-size: 2.5rem;
  margin-top: 0px;
  z-index: 5;
}

.header-title {
  width: 70vw;
  line-height: 1.3;
  font-size: 4rem;
  padding-left: 4px;
  padding-right: 4px;
  color: #ffdbdb;
}

.socials p {
  color: #caccff;
}

.header-body {
  min-width: 45vw;
  width: 85vw;
  display: flex;
  justify-content: center;
}

.button-container {
  margin-top: 0.5vw;
}

.graphics {
  display: flex;
  justify-content: center;
}

.trees {
  position: absolute;
  width: 100vw;
  bottom: -5vw;
  left: 0vw;
  z-index: 1;
}

.trees-small {
  position: absolute;
  width: 100vw;
  bottom: -5vw;
  left: 0vw;
  z-index: 1;
  display: none;
}

.campfire {
  position: absolute;
  bottom: -13vw;
  z-index: 1;
  width: 30vw;
}

.socials {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.8vw;
  max-width: 75vw;
}

/* mobile view - header size */
@media (max-width: 768px) {
  .header-container {
    gap: 7vw;
  }

  .logo {
    width: 85vw;
  }

  .logo-text {
    font-size: 3.4rem;
  }

  .header-content {
    gap: 3vw;
    top: 15vw;
    right: 22vw;
    font-size: 2.8rem;
    padding-left: 2vw;
    padding-right: 2vw;
    gap: 10vw;
  }

  .header-title {
    width: auto;
    line-height: 1.2;
  }

  .header-body {
    width: 85vw;
    line-height: 1.3;
    z-index: 5;
    white-space: normal;
    display: block;
  }
  .tree {
    display: none;
  }
}

@media (max-width: 978px) {
  .trees {
    display: none;
  }

  .trees-small {
    display: block;
  }
}
</style>
