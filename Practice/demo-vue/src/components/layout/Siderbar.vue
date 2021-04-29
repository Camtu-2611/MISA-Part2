<template>
  <div class="sidebar">
    <div class="sidebar__logo">
      <a href="#" class="sidebar__logo-img"></a>
    </div>
    <div class="sidebar__main">
      <div class="sidebar__list scroll-sidebar">
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-home t-icon-menu"></span>
          <span class="sidebar__item-text">Tổng quan</span>
        </a>
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-report t-icon-menu"></span>
          <span class="sidebar__item-text">Báo cáo</span>
        </a>
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-order t-icon-menu"></span>
          <span class="sidebar__item-text">Đơn hàng</span>
        </a>
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-purchase t-icon-menu"></span>
          <span class="sidebar__item-text">Mua hàng</span>
        </a>
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-promotion t-icon-menu"></span>
          <span class="sidebar__item-text">Khuyến mại</span>
        </a>
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-merchandise t-icon-menu"></span>
          <span class="sidebar__item-text">Quản lý cửa hàng</span>
        </a>
      </div>
      <div class="sidebar__bottom">
        <a href="#" class="sidebar__item">
          <span class="sidebar__item-img t-icon-menu"></span>
          <span class="sidebar__item-text">Hàng hóa</span>
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@mixin bg-img($suffix) {
  @if $suffix == home {
    background-position: 0 6px;
  } @else if $suffix == report {
    background-position: 0 -273px !important;
  } @else if $suffix == order {
    background: url("../../assets/images/ic_sogiaohang.png") no-repeat;
    background-position: 4px 9px;
  } @else if $suffix == purchase {
    background-position: 0 -33px;
  } @else if $suffix == proomotion {
    background-position: 0 -196px;
  } @else if $suffix == management {
    background-position: 0 -233px;
  } @else if $suffix == merchandise {
    background-position: 0 -350px;
  }
}

$icon-menu: (
  ic1: home,
  ic2: report,
  ic3: order,
  ic4: purchase,
  ic5: promotion,
  ic6: management,
  ic7: merchandise,
);
.sidebar {
  width: 150px;
  height: 100vh;
  background-color: #2b3173;
  white-space: nowrap;
  z-index: 1;

  &__logo {
    width: 150px;
    height: 52px;
    background-color: #1e235a;
  }

  &__logo-img {
    position: absolute;
    width: 150px;
    height: 50px;
    background-image: url("../../assets/images/Logo_Full_White.png");
    background-repeat: no-repeat;
    background-size: contain;
    background-position-y: 3px;
  }

  &__main {
    width: 100%;
    height: calc(100vh - 52px);
  }
  &__list {
    width: 100%;
    max-height: calc(100% - 52px);
    overflow-y: auto;
  }
  &__item {
    width: 100%;
    height: 40px;
    position: relative;
    display: flex;
    align-items: center;

    &:hover {
      background-color: #1e235a;
      color: #fff;
      cursor: pointer;
    }
  }
  
  .t-icon-menu {
    position: absolute;
    height: 26px;
    width: 22px;
    left: 8px;
    top: 2px;
    text-align: center;
    background: url("../../assets/images/slibarmenu.png") no-repeat;
  }
  @each $key, $ic in $icon-menu {
    .sidebar__item-#{$ic} {
      @include bg-img($ic);
    }
  }
  &__item-text {
    height: 26px;
    width: 100%;
    text-align: left;
    padding-left: 40px;
    line-height: 24px;
  }

  &__bottom {
    border-top: 1px solid #1e235a;
    margin-top: 4px;
  }
}
</style>