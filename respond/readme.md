# Respond
Usefull mixine for control css breakpoints based on screen size or pixel density.

## Usage
Set some variables based on screen size or pixel density:

$mobile: 767px; // means max-width
$tablet: 1025px; // means tablet screen size less than 1025px
$retina: 1.5; // min-device-pixel-ratio:1.5 == min-resolution : 144dpi
$retina-hd: 2.5; // min-device-pixel-ratio:2.5 == min-resolution : 240dpi

Add respond mixin to your mixin file and use as follows:

#header{
  height:100px;
  @include breakpoint($tablet){
    height:50px;
  }
  @include breakpoint($mobile){
    height:auto;
  }
  .logo{
    display:block;
    @include breakpoint($tablet){
        display:inline-block;
        @include breakpoint($retina){
        display:none;
    }
    }
  }
}