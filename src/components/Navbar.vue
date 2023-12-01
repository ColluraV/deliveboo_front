<script>
export default {

}
</script>

<template>


  <nav class="navbar navbar-expand-sm sticky-top">
    <div class="container-fluid align-items-center d-flex justify-content-between">
      <RouterLink class="text-decoration-none logo_text" :to="{ name: 'welcome' }">DeliveBoo</RouterLink>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"><i class="fa-solid fa-bars" style="color: #ffde9f;"></i></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <RouterLink class="btn my-button text-decoration-none" :to="{ name: 'home' }"> Ristoranti </RouterLink>
          </li>          
          <li class="nav-item">
            <RouterLink  :to="{ name: 'about' }" class="btn my-button text-decoration-none">About us</RouterLink>
          </li>
          <li class="nav-item">
                  <a class="btn my-button text-decoration-none" href="http://127.0.0.1:8000/admin/plates">Area Ristoratori</a>
          </li>

        </ul>
        
      </div>
    </div>
</nav>
</template>

<style lang="scss" scoped>
@import '../styles/partials/variables';

.nav-item{
  text-align: end;
}
.my-button {
  background-color: $bg_color_secondary;
  border-radius: 0;
  padding: auto 1.5rem;
  font-weight: 600;
  font-size: 0.8rem;
  color: $gold-text;
  width: 120px;
  height: 100%;

 // // // // // //transition hover buttons// // // // // //
  transition-property: background color;
  transition-duration: 0.7s;
    
  &:hover {
    background: $gold_text;
    border:1px solid $gold-text;
    color: $bg_color;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 30px 60px -12px inset, rgba(0, 0, 0, 0.964) 0px 18px 36px -18px inset;

  }
}

.logo_text {
  color: $gold_text;
  font-weight: bold;
  font-size: 20px;
  text-shadow: 0px 0px 10px rgba(255, 255, 255, 0.516);
  cursor:pointer;
  position:relative;
  padding:10px;
  font-size:28px;
  border-top-right-radius:10px;
  border-bottom-left-radius:10px;
  transition:all 1s;
  &:after,&:before{
    content:" ";
    width:10px;
    height:10px;
    position:absolute;
    border :0px solid #fff;
    transition:all 1s;
    }
  &:after{
    top:-1px;
    left:-1px;
    border-top:5px solid $gold_text;
    border-left:5px solid $gold_text;
  }
  &:before{
    bottom:0px;
    right:0px;
    border-bottom:5px solid $gold_text;
    border-right:5px solid $gold_text;
  }
  &:hover{
    border-top-right-radius:0px;
    border-bottom-left-radius:0px;

    &:before,&:after{
      
      width:105%;
      height:112%;

    }
  }
}

.navbar {
  border-bottom: 1px solid $gold-text;
  background-color: $bg_color_secondary;
}
.navbar-toggler-icon {
    display: inline-block;
    width: auto;
    height: 100%;
    aspect-ratio: 1/1;
    vertical-align: middle;
    color: $gold_text;
    --bs-navbar-toggler-icon-bg:none;
}
</style>




<!--
  
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <RouterLink :to="{ name: 'welcome' }">DeliveBoo</RouterLink>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <RouterLink :to="{ name: 'home' }" >Homepage</RouterLink>
          </li>
          <li class="nav-item">
                  <a href="http://127.0.0.1:8000/dashboard">Area <br> Ristoratori</a>
          </li>

        </ul>
        
      </div>
    </div>
</nav>

-->