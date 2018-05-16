<template>
  <div class="header">
    <div class="header__holder" v-bind:class="{ scrolled: isScrolled }">
      <a href="#" class="logo" v-on:click.stop="logoClick">
        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="180" height="50.031" class="logo__colored"
          aria-hidden="true">
          <defs>
            <filter id="a" x="360" y="280.781" filterUnits="userSpaceOnUse">
              <feImage preserveAspectRatio="none" x="360" y="280.781" width="48.188" height="46.25" result="image" xlink:href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB3aWR0aD0iNDguMTg4IiBoZWlnaHQ9IjQ2LjI1IiB2aWV3Qm94PSIwIDAgNDguMTg4IDQ2LjI1Ij4KICA8ZGVmcz4KICAgIDxzdHlsZT4KICAgICAgLmNscy0xIHsKICAgICAgICBmaWxsOiB1cmwoI2xpbmVhci1ncmFkaWVudCk7CiAgICAgIH0KICAgIDwvc3R5bGU+CiAgICA8bGluZWFyR3JhZGllbnQgaWQ9ImxpbmVhci1ncmFkaWVudCIgeDE9IjI0LjA5NCIgeTE9IjQ2LjI1IiB4Mj0iMjQuMDk0IiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCIgc3RvcC1jb2xvcj0iIzRlYWRiMyIvPgogICAgICA8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiMyOWRlYWEiLz4KICAgIDwvbGluZWFyR3JhZGllbnQ+CiAgPC9kZWZzPgogIDxyZWN0IGNsYXNzPSJjbHMtMSIgd2lkdGg9IjQ4LjE4OCIgaGVpZ2h0PSI0Ni4yNSIvPgo8L3N2Zz4K"
              />
              <feComposite result="composite" operator="in" in2="SourceGraphic" />
              <feBlend result="blend" in2="SourceGraphic" />
            </filter>
          </defs>
          <path d="M395.213 283.445c-.394-2.481-9.472-3.26-15-2.22a27.576 27.576 0 0 0-9.222 3.475c-8.624 4.746-10.764 11.51-11 16.521s2.226 10.891 8.376 16.857c7.031 6.823 13.944 9.5 19.545 8.847s11.276-4.069 16.014-11.934c4.64-7.706 4.851-14.166 3.612-18.024a10.613 10.613 0 0 0-9.279-7.68c-6.518-.673-13.275 1.61-12.564 5.758.513 3 2.956 2.572 7.144 2.087a2.676 2.676 0 0 1 3.038 2.5c.117.811-.8 2.155-2.135 2.669-1.8.692-4.226.745-4.844 2.087-1.752 3.8 1.288 14.627-4.517 14.938-1.94.1-3.539-1.229-4.609-7.743-.408-2.484-.858-5.818-1.611-9.141-1.132-4.989-2.022-6.213-1.828-8.737.182-2.377 1.039-3.96 5.009-6.259a21.175 21.175 0 0 1 6.173-2.035c4.033-.682 7.9-.696 7.698-1.966z"
            transform="translate(-293 -277)" fill="#ffe456" filter="url(#a)" fill-rule="evenodd" />
          <path d="M77.989 7.7a21.218 21.218 0 0 0-7.637 6.507 18.57 18.57 0 0 0-3.368 10.014c-.241 5.011 2.226 10.891 8.376 16.857 7.031 6.823 13.944 9.5 19.545 8.847s11.276-4.069 16.014-11.934c-7.848 13.026-18.237 12.607-31.864 1.251C61.9 24.943 77.989 7.7 77.989 7.7z"
            fill="#299393" fill-rule="evenodd" />
          <path d="M89.484 9.867s-8.676 3.413-8.21 8.512a22.555 22.555 0 0 0 1.477 6.091c.864 2.272 2.409 7.775 2.868 9.616 1.011 4.054 2.678 9.161 5.426 9.414 3.6.247 4.2-6.342 4.692-11.055.239-2.305.358-3.962.974-4.55a3.362 3.362 0 0 1 1.83-.9c1.2-.233 2.474-.037 3.426-.439a2.723 2.723 0 0 0 1.641-2.089c.148-.827-.292-1.778-1.066-3.085 1.1 1.858-.4 3.248-1.56 3.838-1.272.646-2.647.634-3.7 1.083a2.784 2.784 0 0 0-1.4 1c-.51 1.014-.586 3.183-.622 5.564-.062 4.246-.176 9.171-3.649 9.459-1.708.142-2.988-.908-3.695-3.006a27.038 27.038 0 0 1-1.232-5.256c-.261-1.92-.588-3.45-.821-5.007-1.1-7.353-2.623-7.871-2.465-13.019.118-3.49 6.086-6.171 6.086-6.171z"
            fill="#367e87" fill-rule="evenodd" />
          <g class="logo__colored__text">
            <path d="M8.378 20.613a8.432 8.432 0 0 0-4.326 1.118 7.741 7.741 0 0 0-2.983 3.114A9.437 9.437 0 0 0 0 29.358a9.1 9.1 0 0 0 1.1 4.454 8.007 8.007 0 0 0 3.043 3.128 8.568 8.568 0 0 0 4.389 1.133 7.759 7.759 0 0 0 5.561-2.11 1.18 1.18 0 0 0 .372-.847 1.474 1.474 0 0 0-.588-1.134 1.3 1.3 0 0 0-.8-.282 1.911 1.911 0 0 0-1.143.441 5.076 5.076 0 0 1-3.4 1.1 5.422 5.422 0 0 1-2.859-.758 5.173 5.173 0 0 1-1.947-2.092 6.475 6.475 0 0 1-.695-3.036 6.106 6.106 0 0 1 1.484-4.293 4.988 4.988 0 0 1 3.862-1.622 5.212 5.212 0 0 1 2.086.394 4.943 4.943 0 0 1 1.684 1.243 1.543 1.543 0 0 0 1.2.567 1.179 1.179 0 0 0 .712-.222 1.384 1.384 0 0 0 .679-1.164 1.194 1.194 0 0 0-.31-.818 7.622 7.622 0 0 0-6.056-2.83zm17.8-.061a6.841 6.841 0 0 0-2.905.627 6.534 6.534 0 0 0-2.287 1.732v-.6a1.379 1.379 0 0 0-1.545-1.575 1.53 1.53 0 0 0-1.142.41 1.589 1.589 0 0 0-.4 1.165v14.06a1.4 1.4 0 0 0 1.545 1.575 1.525 1.525 0 0 0 1.159-.408 1.641 1.641 0 0 0 .386-1.167v-9.184a3.342 3.342 0 0 1 1.36-2.8 5.743 5.743 0 0 1 3.585-1.037 11.943 11.943 0 0 1 2.009.219 2.454 2.454 0 0 0 .463.063 1.2 1.2 0 0 0 1.235-1 1.128 1.128 0 0 0 .032-.316 1.464 1.464 0 0 0-.927-1.261 5.45 5.45 0 0 0-2.565-.5zm19.128 8.523a10.02 10.02 0 0 0-.927-4.4 7.023 7.023 0 0 0-2.658-2.989 7.669 7.669 0 0 0-4.11-1.068 8.353 8.353 0 0 0-4.31 1.118 7.775 7.775 0 0 0-2.967 3.114 9.426 9.426 0 0 0-1.066 4.513 8.933 8.933 0 0 0 1.128 4.5 8.031 8.031 0 0 0 3.137 3.1 9.3 9.3 0 0 0 7.524.584 8.553 8.553 0 0 0 2.611-1.386 1.146 1.146 0 0 0 .5-.944 1.378 1.378 0 0 0-.557-1.069 1.315 1.315 0 0 0-.927-.316 1.578 1.578 0 0 0-1.019.347 5.76 5.76 0 0 1-1.653.85 5.916 5.916 0 0 1-1.932.345 5.993 5.993 0 0 1-3.971-1.353 5.57 5.57 0 0 1-1.962-3.556h11.742a1.394 1.394 0 0 0 1.02-.392 1.328 1.328 0 0 0 .4-.991zm-7.695-5.756a4.5 4.5 0 0 1 3.307 1.257 5.637 5.637 0 0 1 1.545 3.368h-10.29a5.684 5.684 0 0 1 1.775-3.368 5.3 5.3 0 0 1 3.662-1.257zm17.213-2.706a8.426 8.426 0 0 0-4.342 1.149 8.182 8.182 0 0 0-3.075 3.146 8.986 8.986 0 0 0-1.112 4.45 9.53 9.53 0 0 0 1.036 4.454 7.883 7.883 0 0 0 2.842 3.128 7.44 7.44 0 0 0 4.033 1.133 7.521 7.521 0 0 0 3.337-.755 7.619 7.619 0 0 0 2.627-2.108v1.163a1.569 1.569 0 0 0 .447 1.15 1.626 1.626 0 0 0 2.256 0 1.578 1.578 0 0 0 .448-1.15v-7.015a8.891 8.891 0 0 0-1.127-4.45 8.382 8.382 0 0 0-3.06-3.146 8.26 8.26 0 0 0-4.31-1.149zm0 14.631a5.225 5.225 0 0 1-2.8-.773 5.519 5.519 0 0 1-1.979-2.108 6.192 6.192 0 0 1-.724-3 6.3 6.3 0 0 1 .724-3.021 5.488 5.488 0 0 1 1.979-2.122 5.451 5.451 0 0 1 5.593 0 5.374 5.374 0 0 1 1.962 2.122 6.408 6.408 0 0 1 .711 3.021 6.3 6.3 0 0 1-.711 3 5.4 5.4 0 0 1-1.962 2.108 5.224 5.224 0 0 1-2.8.773zm72.493-14.692a6.83 6.83 0 0 0-2.9.627 6.525 6.525 0 0 0-2.287 1.732v-.6a1.379 1.379 0 0 0-1.545-1.575 1.535 1.535 0 0 0-1.144.41 1.6 1.6 0 0 0-.4 1.165v14.06a1.587 1.587 0 0 0 .4 1.181 1.569 1.569 0 0 0 1.144.394 1.53 1.53 0 0 0 1.159-.408 1.641 1.641 0 0 0 .386-1.167v-9.184a3.337 3.337 0 0 1 1.36-2.8 5.739 5.739 0 0 1 3.585-1.037 11.923 11.923 0 0 1 2.007.219 2.482 2.482 0 0 0 .464.063 1.2 1.2 0 0 0 1.236-1 1.128 1.128 0 0 0 .032-.316 1.467 1.467 0 0 0-.928-1.261 5.445 5.445 0 0 0-2.565-.5zm19.128 8.523a10.02 10.02 0 0 0-.927-4.4 7.021 7.021 0 0 0-2.657-2.989 7.674 7.674 0 0 0-4.11-1.068 8.363 8.363 0 0 0-4.312 1.118 7.777 7.777 0 0 0-2.965 3.114 9.426 9.426 0 0 0-1.067 4.513 8.943 8.943 0 0 0 1.128 4.5 8.025 8.025 0 0 0 3.137 3.1 9.3 9.3 0 0 0 7.525.584 8.547 8.547 0 0 0 2.61-1.386 1.143 1.143 0 0 0 .5-.944 1.377 1.377 0 0 0-.556-1.069 1.32 1.32 0 0 0-.927-.316 1.579 1.579 0 0 0-1.02.347 5.753 5.753 0 0 1-1.654.85 5.906 5.906 0 0 1-1.931.345 6 6 0 0 1-3.971-1.353 5.579 5.579 0 0 1-1.962-3.556h11.743a1.39 1.39 0 0 0 1.019-.392 1.324 1.324 0 0 0 .4-.991zm-7.694-5.756a4.494 4.494 0 0 1 3.306 1.257 5.632 5.632 0 0 1 1.546 3.368H133.31a5.7 5.7 0 0 1 1.778-3.368 5.291 5.291 0 0 1 3.662-1.257zm16.1-2.706a8.862 8.862 0 0 0-3.09.535 5.461 5.461 0 0 0-2.349 1.6 3.934 3.934 0 0 0-.9 2.613q0 3.8 5.933 4.97a9.377 9.377 0 0 1 3.245 1.084 1.908 1.908 0 0 1 .957 1.62 1.818 1.818 0 0 1-.973 1.606 5.226 5.226 0 0 1-2.734.6 6.482 6.482 0 0 1-2.5-.489 4.771 4.771 0 0 1-1.761-1.149 1.641 1.641 0 0 0-1.175-.567 1.863 1.863 0 0 0-1.081.441 1.472 1.472 0 0 0-.618 1.228 1.347 1.347 0 0 0 .4.973 7.57 7.57 0 0 0 2.905 1.732 11.68 11.68 0 0 0 3.955.66 8.716 8.716 0 0 0 3.6-.678 5.136 5.136 0 0 0 2.27-1.856 4.69 4.69 0 0 0 .773-2.624 4.013 4.013 0 0 0-1.406-3.177 10.665 10.665 0 0 0-4.774-1.922 14.6 14.6 0 0 1-2.5-.706 2.762 2.762 0 0 1-1.174-.786 1.748 1.748 0 0 1-.31-1.055 1.5 1.5 0 0 1 .913-1.367 4.88 4.88 0 0 1 2.332-.489 6.4 6.4 0 0 1 2.1.3 4.564 4.564 0 0 1 1.638 1.022 2.1 2.1 0 0 0 1.452.6 1.41 1.41 0 0 0 .866-.253 1.264 1.264 0 0 0 .526-.976 1.62 1.62 0 0 0-.4-1.006 6.136 6.136 0 0 0-2.517-1.822 9.257 9.257 0 0 0-3.6-.663zm17.707-.032a7.714 7.714 0 0 0-2.906.551 6.824 6.824 0 0 0-2.347 1.56v-7.71a1.6 1.6 0 0 0-.433-1.165 1.688 1.688 0 0 0-2.271 0 1.566 1.566 0 0 0-.449 1.165v21.391a1.574 1.574 0 0 0 .449 1.15 1.644 1.644 0 0 0 2.271 0 1.608 1.608 0 0 0 .433-1.15V27.5a3.628 3.628 0 0 1 .6-2.045 4.225 4.225 0 0 1 1.668-1.447 5.207 5.207 0 0 1 2.365-.534 4.9 4.9 0 0 1 3.568 1.306 5.133 5.133 0 0 1 1.345 3.854v7.737a1.574 1.574 0 0 0 .448 1.15 1.624 1.624 0 0 0 2.255 0 1.578 1.578 0 0 0 .449-1.15v-7.737a9.2 9.2 0 0 0-.958-4.356 6.622 6.622 0 0 0-2.657-2.755 7.773 7.773 0 0 0-3.832-.944z"
              fill-rule="evenodd" fill="#292f39" />
          </g>
          <g>
            <path d="M71.76 44.032a1.421 1.421 0 1 1-1.392 1.418 1.405 1.405 0 0 1 1.392-1.418z" fill="#31d3ac" fill-rule="evenodd" />
            <path d="M119.039 12.593a1.734 1.734 0 1 1-1.7 1.734 1.716 1.716 0 0 1 1.7-1.734z" fill="#2addaa" fill-rule="evenodd" />
            <circle cx="109.922" cy="3.781" r="3.703" fill="#2adcaa" />
          </g>
        </svg>

        <svg xmlns="http://www.w3.org/2000/svg" width="115" height="32" viewBox="0 0 115 32" class="logo__black" aria-hidden="true">
          <path fill="#000" d="M45.899 28.163c0.005-0 0.012-0 0.018-0 0.502 0 0.909 0.407 0.909 0.909s-0.407 0.909-0.909 0.909c-0.502 0-0.909-0.407-0.909-0.909 0-0.001 0-0.001 0-0.002v0c-0-0.002-0-0.005-0-0.008 0-0.494 0.398-0.894 0.891-0.899h0z"></path>
          <path fill="#000" d="M76.138 8.055c0.006-0 0.014-0 0.022-0 0.613 0 1.109 0.497 1.109 1.109s-0.497 1.109-1.109 1.109c-0.612 0-1.109-0.496-1.109-1.109v0c-0-0.003-0-0.006-0-0.010 0-0.603 0.485-1.093 1.087-1.099h0.001z"></path>
          <path fill="#000" d="M72.675 2.418c0 1.308-1.060 2.368-2.368 2.368s-2.368-1.060-2.368-2.368c0-1.308 1.060-2.368 2.368-2.368s2.368 1.060 2.368 2.368z"></path>
          <path fill="#000" d="M65.376 4.122c-0.251-1.587-6.058-2.085-9.594-1.42-2.222 0.414-4.202 1.188-5.977 2.267l0.078-0.044c-5.516 3.037-6.885 7.362-7.036 10.567s1.423 6.966 5.357 10.782c4.497 4.364 8.919 6.076 12.5 5.659s7.213-2.603 10.243-7.633c2.968-4.929 3.102-9.059 2.311-11.528-0.777-2.681-3.095-4.654-5.908-4.91l-0.026-0.002c-4.168-0.43-8.491 1.030-8.036 3.683 0.328 1.919 1.89 1.645 4.569 1.335 0.070-0.010 0.152-0.016 0.234-0.016 0.911 0 1.656 0.712 1.709 1.611l0 0.005c0.075 0.519-0.512 1.378-1.366 1.707-1.151 0.443-2.702 0.477-3.099 1.334-1.12 2.43 0.824 9.355-2.888 9.555-1.24 0.064-2.264-0.787-2.948-4.952-0.261-1.589-0.549-3.722-1.030-5.847-0.724-3.192-1.293-3.974-1.169-5.588 0.117-1.52 0.666-2.533 3.204-4.003 1.142-0.598 2.468-1.051 3.868-1.29l0.080-0.011c2.58-0.436 5.054-0.445 4.924-1.257z"></path>
        </svg>
      </a>

      <button v-on:click="menuBtnToggle" class="menu-btn">
        <span></span>
      </button>
    </div>
    <div class="header__navigation">
      <navigation/>
    </div>
  </div>
</template>

<script>
import Navigation from "@/components/Navigation.vue";

export default {
  components: {
    Navigation
  },

  data() {
    return {
      scrolled: false,
      isScrolled: false
    };
  },

  methods: {
    menuBtnToggle: function(event) {
      document.body.classList.toggle("is-nav-opened");
    },
    logoClick: event => {
      event.preventDefault();
    },
    handleScroll() {
      this.scrolled = window.scrollY;
      if (this.scrolled >= 200) {
        this.isScrolled = true;
      }
    }
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>


<style lang="scss">
.header__holder {
  padding-top: 7px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  z-index: 100;
  padding-left: 4px;
  padding-right: 10px;
  transition: background-color 0.3s;
  &.scrolled {
    background-color: $light;
  }
  @include tablet {
    padding-top: 17px;
    padding-left: 13px;
    padding-right: 20px;
  }
  @include desktop-s {
    padding-top: 36px;
    padding-left: 33px;
    padding-right: 50px;
  }
  @include desktop-m {
    padding-top: 40px;
  }
  @include desktop-l {
    padding-top: 27px;
  }
}

// logo styles
.logo {
  display: block;
  width: 180px;
  position: relative;
  overflow: hidden;
  transform: translateX(-60px);
  transition: transform 0.5s;
  margin-top: 3px;
  &:hover {
    transform: translateX(0);
    .logo__colored {
      opacity: 1;
    }
    .logo__black {
      opacity: 0;
    }
    .logo__colored__text {
      opacity: 1;
    }
  }
}

.logo__black {
  width: 180px;
  height: 50px;
  position: absolute;
  top: 0;
  left: 0;
  transition: opacity 0.3s;
}

.logo__colored {
  opacity: 0;
  transition: opacity 0.3s;
}

.logo__colored__text {
  opacity: 0;
  transition: opacity 0.4s 0.2s;
}
// /logo styles

// menu btn styles
.menu-btn {
  height: 20px;
  position: relative;
  width: 40px;
  padding: 0;
  text-indent: -9999px;
  border: none;
  background-color: transparent;
  &:focus {
    outline: none;
  }

  span {
    width: 40px;
    height: 2px;
    background-color: $dark;
    left: 0;
    top: 9px;
    position: absolute;
    border-radius: 2px;
    &::before,
    &::after {
      content: "";
      position: absolute;
      right: 0;
      width: 100%;
      height: 2px;
      border-radius: 2px;
      transition: transform 0.3s;
      background-color: $dark;
    }
    &::before {
      top: -9px;
      transition-property: top, transform;
    }
    &::after {
      bottom: -9px;
      transition-property: bottom, transform;
      width: 28px;
    }
  }
  @include desktop-s {
    span,
    & span::before,
    & span::after {
      transition: background-color 0.5s;
    }
  }
  &:hover {
    cursor: pointer;
    span,
    & span::before,
    & span::after {
      background-color: $brand-color;
    }
  }
}
// /menu btn styles

.header__navigation {
  position: fixed;
  padding-top: 76px;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 20;
  height: 100vh;
  overflow: auto;
  background-color: $light;
  transform: translateY(-200%);
  transition: transform 0.3s;
}

// menu opened styles
.is-nav-opened {
  .menu-btn {
    span {
      background: none;
      width: 0;
      margin: 0 auto;
      &::before,
      &::after {
        width: 24px;
        left: 16px;
      }
      &::before {
        top: 0;
        transform: rotate(45deg);
      }
      &::after {
        bottom: 0;
        transform: rotate(-45deg);
      }
    }
  }

  .header__navigation {
    transform: translateY(0);
  }
}
// /menu opened styles
</style>
