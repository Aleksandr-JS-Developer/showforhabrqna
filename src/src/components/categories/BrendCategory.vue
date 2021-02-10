<template>
<div class="brends">
    <button
        v-for="( item, i ) in allBrends"
        :key="i"
        :class="{
            brendBttn: true,
            active: brandsActive.indexOf( item ) !== -1,
            'menu-button': true,
            screen: !this.touchScreen
        }"
        @click="selectIt( item )"
    >{{ item }}
        <span
            class="B_checkmark"
            v-if="brandsActive.indexOf( item ) !== -1 && !touchScreen"
        > <img src="https://img.icons8.com/ios/13/000000/checkmark.png"/>
        </span>
    </button>
</div>
  
</template>

<script>
    export default {
        name: 'BrendCategory',
        props: ['allBrends', 'brandsActive'],
        data(){
            return {
                touchScreen: false
            }
        },
        methods: {
            selectIt( category ){   
                this.$emit( 'toggledCategory', category );
            }
        },
        mounted(){
            this.touchScreen = ( /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test( navigator.userAgent ) );
        }
    }
</script>

<style>

    .brends {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
    }

    .brendBttn {
        width: 100%;
        font-size: 12px;
        text-align: right;
        border: 1px solid transparent;
        background-color: transparent;
        text-transform: uppercase;
        letter-spacing: 0.45em;
        color: #999;
        transition: 2s;

        margin-bottom: 12%;
    }
    .brendBttn.screen:hover {
        transition: 0.15s;
        color: #565454;
    }
    .brendBttn.active {
        color: black;
    }
    .B_checkmark {
        margin-left: -8px;
        margin-right: -13px;
    }
</style>