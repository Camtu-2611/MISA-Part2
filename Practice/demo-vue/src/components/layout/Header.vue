<template>
  <div class="header">
    <div class="header__left">Cửa hàng</div>
    <div class="header__right">
      <div class="header__mid">
        <div class="header__select store-catalog">
          <select class="select-arrow-down" id="list-store" name="list-store">
            <option value="0">Chuỗi cửa hàng</option>
            <option value="1">DODAVI-160 Hoàng Hoa Thám</option>
            <option value="2">SENLIVE-175 Đường Láng</option>
            <option value="3">HENCI-24 Trản Quốc Hoàn</option>
          </select>
        </div>
        <div class="header__select div-user">
          <button id="user-button" class="t-btn">
            <!-- <span class="user__icon"></span> -->
            <span class="user__account">Ngô Thị Cẩm Tú</span>
            <div class="icon-drop">
              <!-- <i class="fas fa-angle-down"></i> -->
            </div>
          </button>
          <div class="user-setting" id="user-setting">
            <ul class="setting-list">
              <li class="setting-item">
                <a href="#" class="account">Tài khoản</a>
              </li>
              <li class="setting-item">
                <a href="#" class="change-password">Thay đổi mật khẩu</a>
              </li>
              <li class="setting-item">
                <a href="#" class="logout">Đăng xuất</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="header__button">
        <div
          class="div-btn support"
          title="Tổng đài MISA - liên hệ để được hỗ trợ"
        >
          <button class="t-btn btn-header btn-support"></button>
        </div>
        <div class="div-btn notify" title="Thông báo">
          <button class="t-btn btn-header btn-notify">
            <i class="fa-bell">
              <span class="item-head-notify"></span>
            </i>
          </button>
        </div>
        <div class="div-btn help" title="Trợ giúp">
          <button class="t-btn btn-header btn-help"></button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  width: 100%;
  height: 52px;
  background-color: #ffffff;
  color: #212121 !important;
  align-items: center;
  justify-content: space-between;

  .header__left {
    width: 122px;
    height: 52px;
    overflow: hidden;
    font-weight: 600;
    font-size: 1.1rem;
    line-height: 52px;
    margin-left: 21px;
  }

  .header__right {
    display: flex;
    position: relative;
    width: calc(100% - 122px);
    justify-content: flex-end;
    align-items: center;

    .header__mid {
      display: flex;
      overflow: hidden;
      align-items: center;
      font-size: 13px !important;

      .header__select {
        height: 32px;
        line-height: 30px;
        margin: 0 7px;
        box-sizing: border-box;
      }
      .store-catalog {
        border: 1px solid #d0d0d0;
        border-radius: 3px;
      }

      #list-store {
        padding: 0 4px 2px 6px !important;
        width: 200px;
        &:hover{
            cursor: pointer;
        }
      }

      .div-user {
        white-space: nowrap;
        .icon-drop{
            width: 18px;
            height: 18px;
            background-image: url("../../assets/images/arrow-down-line.png");
            background-repeat: no-repeat;
            background-size: 10px;
            background-position-y: center;
            margin-left: 8px;
        }
      }
      #user-button {
        display: flex;
        height: 32px;
        background: url("../../assets/images/user.png") no-repeat;
        background-position: 0 2px;
        background-size: 28px;
        padding-left: 36px;
        font-weight: 700;
        font-size: 13px;
        align-items: center;

        &:hover{
            cursor: pointer;
        }
      }
    }

    .header__button {
      display: flex;
      margin-left: 4px;
      .div-btn {
        height: 52px;
        width: 50px;
      }

      .support {
        width: 46px;
        box-sizing: border-box;
      }
      .btn-header {
        height: 100%;
        width: 100%;
        border-left: 1px solid #e1e1e1;
        
        background-position: center;
        &:hover{
            cursor: pointer;
        }
      }

      .btn-support {
        background-image: url("../../assets/images/misasupport_1.png");
        background-repeat: no-repeat;
        background-color: #2b3173 !important;
        background-position: unset;
        border: 1px solid #5897ce;
      }
      .btn-notify{
        position: relative;
        background-image: url("../../assets/images/notify-18.png");
        background-repeat: no-repeat;

        &:hover{
        background-image: url("../../assets/images/notify-hover-18.png");
        }

        .item-head-notify{
            height: 8px;
            width: 8px;
            background-color: #ffa500f2;
            border-radius: 50%;
            position: absolute;
            top: 15px;
            right: 14px;
        }
      }

      .btn-help{
        background-image: url("../../assets/images/icon_help_18.png");
        background-repeat: no-repeat;

        &:hover{
        background-image: url("../../assets/images/icon-help-18-hover.png");
        }
      }

    }
  }
}
</style>