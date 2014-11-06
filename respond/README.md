# Respond
Usefull mixine for control css breakpoints based on screen size or pixel density.

## Usage
Set some variables based on screen size or pixel density:
<pre>
  $mobile: 767px; // means max-width
  $tablet: 1025px; // means tablet screen size less than 1025px
  $retina: 1.5; // min-device-pixel-ratio:1.5 == min-resolution : 144dpi
  $retina-hd: 2.5; // min-device-pixel-ratio:2.5 == min-resolution : 240dpi
</pre>

Add respond mixin to your mixin file and use as follows:

<pre>
  @include breakpoint($tablet){
    /* Tablet-specific stuff here */ 
  }
  @include breakpoint($mobile){

    /* Mobile-specific stuff here */ 

    @include breakpoint($retina){

      /* Mobile Retina-specific stuff here */ 

    }
  }
</pre>

See `usage.scss` for a more demo