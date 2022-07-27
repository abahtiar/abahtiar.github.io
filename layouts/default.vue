<template>
        <!-- main content -->
       <div class="container">
            <Transition>
                <NavMenu v-if="state.showMenu" v-on:show-menu="setShowMenu(to)" ></NavMenu>
            </Transition>
             <!-- nutton nav menu open -->
            <button class="btn-icon-menu" @click="setShowMenu(true)">
              <svg width="40" height="40" clip-rule="evenodd" fill-rule="evenodd" stroke-linejoin="round" stroke-miterlimit="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="m11 16.745c0-.414.336-.75.75-.75h9.5c.414 0 .75.336.75.75s-.336.75-.75.75h-9.5c-.414 0-.75-.336-.75-.75zm-9-5c0-.414.336-.75.75-.75h18.5c.414 0 .75.336.75.75s-.336.75-.75.75h-18.5c-.414 0-.75-.336-.75-.75zm4-5c0-.414.336-.75.75-.75h14.5c.414 0 .75.336.75.75s-.336.75-.75.75h-14.5c-.414 0-.75-.336-.75-.75z" fill-rule="nonzero"/></svg>
            </button>
            <main>
                <NuxtPage />
            </main>
       </div>
        <!-- footer -->
        <Footer></Footer>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap');
*{
    box-sizing: border-box;
}
body{
    background: #D9D9D9;
    font-family: 'Lato', sans-serif;
    font-weight: 400;
}
.container{
    background: white;
    border-radius: 15px;
    width: 96%;
    margin: 30px 2%;
    padding: 30px;
    position: relative;
    min-height: 80vh;
    margin-bottom: 150px;
}
.btn-icon-menu{
    border: 0;
    background: none;
    position: absolute;
    top: 60px;
    right: 60px;
    cursor: pointer;
}
@media screen and (max-width:769px){
    .btn-icon-menu{
        top: 30px;
        right: 30px;
    }
    .container{
        min-height: 85vh;
        margin-bottom: 120px;
    }
}
</style>

<script setup>
const state = reactive({
  showMenu: false,
})
const setShowMenu = (to) =>{
  state.showMenu = to
}
</script>