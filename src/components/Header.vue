<template>
    <!-- begin header -->
    <div class="header">
        <div class="mob-nav js-mob-nav">
            <span></span>
        </div>
        <div class="header__logo">
            <a href="#" class="logo">
                <img src="img/logo.svg" alt="PoweredTemplate">
            </a>
        </div>
        <div class="header__user">
            <dropdown-button text="My Button">
                <li><a href="">afsf</a></li>
                <li><a href="">af</a></li>
                <li><a href="">asfasf</a></li>
            </dropdown-button>
            <div class="user">
                <div class="user__drop">
                    <div class="account js-dropdown" >
                        <!-- <div class="account__image">{{mixins.icon('user')}}</div> -->
                        <div class="account__name">Vasiliy Kovalenko</div>
                        <!-- <div class="account__arrow">{{mixins.icon('arrow')}}</div> -->
                        <div class="account__dropdown js-dropdown-links">
                            <ul class="account__links">
                                <li class="js-popup-link" data-popup="change-pass"><a href="#">Change password</a></li>
                                <li class="js-popup-link" data-popup="update-profile"><a href="#">Update Profile</a></li>
                                <li class="js-popup-link" data-popup="ico-info"><a href="#">2FA</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="user__logout">
                    <a href="#" class="logout">
                        <!-- <div class="logout__icon">{{mixins.icon('logout')}}</div> -->
                        <div class="logout__text">Logout</div>
                    </a>
                </div>
            </div>
        </div>
    </div>
    <!-- end header -->
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

// @Component
// export default class Header extends Vue {
//   @Prop() private msg!: string;
// }

// var dropdownAccount = $('.js-dropdown');
//   var dropdownMenu = $(dropdownAccount).find('.js-dropdown-links');
//   $(dropdownAccount).click(function(e) {
//     e.stopPropagation();
//     dropdownAccount.toggleClass('is-open');
//     dropdownMenu.slideToggle('fast');
//   });
//   $(dropdownMenu).click(function(e) {
//     e.stopPropagation();
//   });
</script>

<style lang="sass">

.header
    // +clr
    padding: 25px 19px 21px 32px
    background-color: #fff
    border-bottom: 1px solid #dedede
    &:after
        content: ''
        display: table
        clear: both
    &__logo
        float: left
        width: 296px
        height: 30px
    &__user
        float: right
        padding-top: 5px
.user
    display: flex
    font-size: 16px
    color: #ccc
    font-size: 16.67px
    &__logout
        margin-left: 55px
    svg
        fill: #ccc
    a
        color: #000
        text-decoration: none
.account
    cursor: pointer
    display: flex
    position: relative
    &__image
        font-size: 20px
    &__name
        margin-right: 27px
        margin-left: 18px
        line-height: 1.2
        &:hover
            color: red
    &__dropdown
        display: none
        position: absolute
        top: 50px
        right: 0
        z-index: 1000
        background-color: #fff
        padding: 15px 20px
        border-bottom: 1px solid #ccc
        li
            &:not(:last-child)
                margin-bottom: 30px
            &:hover
                a
                    color: red
        a
            // +sfM
            font-size: 14.58px
            color: #ccc
.logout
    display: flex
    &__text
        margin-left: 18px
        line-height: 1.2
        // +sm
        //     display: none
    &__icon
        font-size: 20px
</style>