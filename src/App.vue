<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
  *:focus{
    outline: none;
  }
  body{
    margin: 0;
    font-family: W95f;
  }
  @font-face {
    font-family: 'W95f';
    src: url('../public/px_sans_nouveaux.ttf'); /* IE9 Compat Modes */
  }
  .btn{
    background-color: #D4D3C9;
    border-top: 2px solid #F9FBEB;
    border-left: 2px solid #F9FBEB;
    border-bottom: 2px solid #868872;
    border-right: 2px solid #868872;
    width: 8rem;
    padding: .5rem .2rem;
  }
  .btn:active{
    background-color: #909085;
    border-bottom: 2px solid #F9FBEB;
    border-right: 2px solid #F9FBEB;
    border-top: 2px solid #868872;
    border-left: 2px solid #868872;
  }
  .form{
    background-color: #fff;
    border: 2px solid #000;
    padding: .5rem;
    color: #000;
    font-family: 'W95f';
    caret-shape: block;
  }
</style>
