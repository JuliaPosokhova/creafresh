<template>
  <div class="footer">
    <div class="container">
      <div class="footer__holder">
        <div class="footer__item">
          <div class="footer__info">
            <address> Creafresh Design Agency, 18000 Ukraine, Cherkassy, Il’ina st, ap 245 - 23</address>
          </div>
          <div class="footer__info">
            <a href="tel:+38(063) 374 44 62 " class="footer__link">+38(063) 374 44 62 </a>
            <a href="mailto:info@creafresh.com" class="footer__link"> info@creafresh.com </a>
          </div>
        </div>
        <div class="footer__item">
          <ul class="socials">
            <li>
              <a href="#" class="socials__link instagram">Instagram </a>
            </li>
            <li>
              <a href="#" class="socials__link facebook"> Facebook</a>
            </li>
          </ul>
          <div class="footer__copyright">
            © CreaFresh 2015-2018. All rights reserved.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.footer {
  font-size: 14px;
  line-height: 28px;
  font-weight: 700;
  text-align: center;
  padding-top: 40px;
  padding-bottom: 40px;
  border-top: 1px solid #e9e9ea;
  @include desktop-s {
    text-align: left;
    padding-top: 78px;
    padding-bottom: 80px;
  }
  .container {
    @include desktop-l {
      max-width: 100%;
    }
  }
}

.footer__holder {
  @include desktop-s {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

.footer__link {
  color: initial;
  text-decoration: none;
  transition: color 0.3s;
  &:active {
    color: $brand-color;
  }
  &:hover {
    @include desktop-s {
      color: $brand-color;
    }
  }
}

.socials {
  display: flex;
  justify-content: center;
  padding-top: 30px;
  padding-bottom: 10px;
  @include desktop-s {
    justify-content: flex-end;
    font-size: 14px;
    line-height: 50px;
    padding-bottom: 0;
    padding-top: 0;
  }
}

.socials__link {
  text-decoration: none;
  padding-left: 7px;
  padding-right: 7px;

  @include desktop-s {
    &:hover {
      text-decoration: underline;
    }
  }
  &.instagram {
    color: #c536a5;
  }
  &.facebook {
    color: #475993;
  }
}

.footer__item {
  @include desktop-s {
    width: auto;
  }
}

.footer__copyright {
  font-size: 12px;
  @include desktop-s {
    text-align: right;
  }
}
</style>
