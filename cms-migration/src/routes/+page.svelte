<script>
import { onMount } from 'svelte';
import Music from './Music.svelte';
import Photos from './Photos.svelte';
import Videos from './Videos.svelte';
import Bio from './Bio.svelte';

/**
 * @type {any}
 */
let content;

async function loadContent() {
    const response = await fetch('https://shanti.maxelia.com/content');
    const json = await response.json();
    content = json;
}

onMount(async () => {

(function($){
    "use strict";

$.fn.mobilecheck = function () {
    var check = false;
    (function(a){if(/(android|ipad|playbook|silk|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows (ce|phone)|xda|xiino/i.test(a)||/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0,4)))check = true})(navigator.userAgent||navigator.vendor||window.opera);
    return check;
}

$.fn.qtParallax = function(){
    $('.parallax').parallax();
}

$.fn.qtparticlesJs = function(){
    if($("body").hasClass("mobile")){
        return;
    }
    $(".qt-particles").each(function(i,c){
        var that= $(this),
            boxid = that.attr("id");
        console.log(boxid);
        particlesJS(boxid, {
            "particles": {
                "number": {
                    "value": 160,
                    "density": {
                        "enable": true,
                        "value_area": 800
                    }
                },
                "color": {
                    "value": !that.attr("data-color") ? "#FFFFFF" : that.attr("data-color")
                },
                "shape": {
                    "type": "polygon",
                    "stroke": {
                        "width": 0,
                        "color": "#000000"
                    },
                    "polygon": {
                        "nb_sides": 3
                    }
                },
                "opacity": {
                    "value":  !that.attr("data-opacity") ? "0.5" : that.attr("data-opacity"),
                    "random": true,
                    "anim": {
                        "enable": true,
                        "speed": 1,
                        "opacity_min": 0,
                        "sync": false
                    }
                },
                "size": {
                    "value": 5,
                    "random": true,
                    "anim": {
                        "enable": false,
                        "speed": 50,
                        "size_min": 0.1,
                        "sync": false
                    }
                },
                "line_linked": {
                    "enable": that.attr("data-lines") ? true : false,
                    "distance": 150,
                    "color": !that.attr("data-color") ? "#FFFFFF" : that.attr("data-color"),
                    "opacity": !that.attr("data-opacity") ? "0.5" : that.attr("data-opacity"),
                    "width": 1
                },
                "move": {
                    "enable": true,
                    "speed": !that.attr("data-speed") ? 1 : that.attr("data-speed"),
                    "direction": "none",
                    "random": true,
                    "straight": false,
                    "out_mode": "out",
                    "bounce": false,
                    "attract": {
                        "enable": false,
                        "rotateX": 600,
                        "rotateY": 1200
                    }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                    "onhover": {
                        "enable": false,
                        "mode": "grab"
                    },
                    "onclick": {
                        "enable": true,
                        "mode": "push"
                    },
                    "resize": true
                },
                "modes": {
                    "grab": {
                        "distance": 140,
                        "line_linked": {
                            "opacity": 1
                        }
                    },
                    "bubble": {
                        "distance": 400,
                        "size": 40,
                        "duration": 2,
                        "opacity": 8,
                        "speed": 3
                    },
                    "repulse": {
                        "distance": 200,
                        "duration": 0.4
                    },
                    "push": {
                        "particles_nb": 4
                    },
                    "remove": {
                        "particles_nb": 2
                    }
                }
            },
            "retina_detect": true
        });
    });
}

$.fn.qtSmoothScroll = function(){
    var body = $("body");
    body.off("click",'a.qwsmoothscroll');
    body.on("click",'a.qwsmoothscroll', function(e){     
        e.preventDefault();
        $('html,body').animate({scrollTop:$(this.hash).offset().top - 70}, 800);
    });
}
$.fn.parallaxPolydecor = function(){
    if($("body").hasClass("mobile")){
        return;
    }
    if($(".qt-polydecor").length < 1 && $(".qt-polydecor-page").length < 1){
        return;
    }
    var element1, element2, scrollTop;
    $('.qt-polydecor').not(".nopoly").each(function(){
        var container = $(this);
        container.wrapInner( "<div class='qt-polydecor-content'></div>");
        container.append('<div class="decor1"></div><div class="decor2"></div>');
        element1 = container.find(".decor1"),
        element2 = container.find(".decor2"); // assigning the object 
        var $this = $(this);
        var scrollTop = $(window).scrollTop();
        var offset = $this.offset().top;
        var height = $this.outerHeight();
        var speed1 = 100;
        var speed2 = 130;
        var scrollTop;
        var  offset = $this.offset().top,
        height = $this.outerHeight();
    });
    function updatePolydecor(e) {
        scrollTop = window.pageYOffset;
        $('.qt-polydecor, .qt-polydecor-page > .kc_row, .qt-polydecor-page > .vc_row').each(function(){
            var $this = $(this),
            offset = $this.offset().top,
            yBgPosition = Math.round((offset - scrollTop) );

            $this.find(".decor1").css({top: (yBgPosition * 0.98) +"px"});
            $this.find(".decor2").css({top: (yBgPosition * 0.6) +"px"});

        });
    }
    updatePolydecor();
    window.addEventListener('scroll', updatePolydecor, false);
    return true;
}

$.fn.qwInitPage = function(){

    // Materializecss parallax http://materializecss.com/parallax.html
    $.fn.qtParallax();

    // Sticky js http://stickyjs.com/
    $("#stickymenu").sticky({topSpacing:0, responsiveWidth: true, zIndex: 100});

    $(".modal-trigger").on("click",function(e){
        e.preventDefault();
        if($(this).attr("data-iframe") !== undefined) {
            $("#modalframe").attr("src", $(this).attr("data-iframe"));
        }
        return true;
    });

    //  initialize the modal window of the album
    $('.modal-trigger').leanModal();

    //  initialize the animated background polygons
    $.fn.parallaxPolydecor();

    // background particles
    $.fn.qtparticlesJs();

    // smooth internal links scrolling
    $.fn.qtSmoothScroll();

    // http://materializecss.com/scrollspy.html
    $('.scrollspy').scrollSpy();

    // mobile navigation
    $('.button-collapse').sideNav({
          menuWidth: 300, // Default is 240
          edge: 'right', // Choose the horizontal origin
          closeOnClick: true // Closes side-nav on <a> clicks, useful for Angular/Meteor
        }
      );

    // video lightbox
    $( '.swipebox' ).swipebox();

    // materializecss slideshow
    $('.slider').slider();

    jQuery(window).load(function() {
        if(false === $.fn.mobilecheck()) {
            var s = skrollr.init();
        }
    });
}


/**====================================================================
 *
 *
 *	Page Ready Trigger
 * 	This needs to call only $.fn.qtInitTheme
 * 
 ====================================================================*/
$.fn.qwInitPage();

})(jQuery);
    })
</script>

<header id="home" class="qt-header parallax-container scrollspy" >
    <div class="parallax" data-start="" data-end=""><img src="images/sp/ShantiVinyl.png"  alt="background"></div>
    <div class="qt-valign-wrapper">
        <div class="qt-valign">
            <div class="container center-align">
        <!--<img src="images/SP_rOLLINGoN_WEB_03X.png" class="logo" alt="Logo">-->

                <h4>11 PIECE | REGGAE | RAP | SKA | CROSSOVER</h4>
            </div>
        </div>
    </div>
    <div class="qt-particles" id="particlesheader" data-color="#00FFB0" data-opacity="0.5" data-speed="1"> </div>
</header>
<!-- ====================== HEADER END ================================================ -->


<!-- ====================== MENU ================================================ -->
<div id="menu" class="qt-menu-wrapper" data-0-top>
    <nav id="stickymenu" class="qt-menu shades-text text-white"  >
        <!-- desktop menu -->
        <ul class="qt-desktopmenu">
            <li><a href="#home" class="qwsmoothscroll">Home</a></li>
            <li><a href="#music" class="qwsmoothscroll">Music</a></li>
            <li><a href="#video" class="qwsmoothscroll">Videos</a></li>
            <li><a href="#photos" class="qwsmoothscroll">Photos</a></li>
            <li><a href="#bio" class="qwsmoothscroll">Dates &amp; Bio</a></li>
            <li><a href="#booking" class="qwsmoothscroll">Contact</a></li>
            <li><a href="#presskit" class="qwsmoothscroll">Shop</a></li>

        </ul>
        <!-- mobile menu -->
        <ul id="slide-out" class="side-nav qt-mobilemenu">
            <li><a href="#home" class="qwsmoothscroll">Home</a></li>
            <li><a href="#music" class="qwsmoothscroll">Music</a></li>
            <li><a href="#video" class="qwsmoothscroll">Videos</a></li>
            <li><a href="#photos" class="qwsmoothscroll">Photos</a></li>
            <li><a href="#bio" class="qwsmoothscroll">Dates &amp; Bio</a></li>
            <li><a href="#booking" class="qwsmoothscroll">Contact</a></li>
            <li><a href="#presskit" class="qwsmoothscroll">Crowdfunding</a></li>

        </ul>
        <a href="#" data-activates="slide-out" class="button-collapse qt-menu-switch"><span class="lnr lnr-menu"></span></a>
    </nav>
</div>
        <main class="qt-main">
            {#await loadContent() then}
            <Music music={content.music}/>
            <Videos videos={content.videos} />
            <Photos photos={content.photos} />
            <Bio bio={content.bio}/>
            {/await}
            
            <div id="booking" class="section section-booking qt-fullscreen scrollspy  qt-polydecor poly3">
                <div class="qt-valign-wrapper">
                    <div class="qt-valign flow-text">
                        <h2 class="qt-section-title" data-100p-top="opacity:0;" data-70p-top="opacity:1;">CONTACT<i class="deco"></i></h2>
                        <div class="qt-booking-form">
                              <div id="contacts" class="row qt-contacts">
                                  <div class="col s12">
                                      <h4 class="center-align">Keep the Shantis in Contact</h4>
                                      <p><span class="lnr lnr-smartphone"></span><span> +39 347 74 26 390 <br> +39 333 52 65 182 </span></p>
                                      <p><span class="lnr lnr-pencil"></span><span>info@shantipowa.com</span></p>
                                        <br>
                                        <br>

                                  </div>
                              </div>
                        </div>
                    </div>
                </div>
            </div>
           
            <div id="presskit" class="section section-presskit parallax-container scrollspy" >
                <div class="parallax"><img src="images/parallax3.jpg" alt="background"></div>
                <div class="qt-polydecor poly4">
                        <div class="container">
                            <div class="qt-framed center-align"   data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-30p-top="opacity:1;" >
                                <h2 class="qt-section-title">Shop<i class="deco"></i></h2>
                                <img src="images/sp_merch.jpg" width="720" alt="background">
                                <h4 class="center-align"><a href="https://shantipowarecords.bandcamp.com/merch">Shanti Powa Records Shop</a></h4>
                            </div>
                        </div>
                    </div>
                <div class="qt-particles" id="particlesbio" data-color="#00FFB0" data-opacity="0.9" data-speed="1"></div>
            </div>
        </main>
    <footer class="qt-footer parallax-container blue-grey-text text-lighten-5">
    <div class="parallax"><img src="images/parallax3.jpg" alt="background"></div>
    <div class="container center-align">
        <h3 class="qt-footertitle"><img src="images/sp/shantipowa_logo.png" width="300" alt="Shanti Powa OFFICIAL"></h3>
        <h5><a href="#home" class="qwsmoothscroll">Shanti Powa</a><br>11 PIECE | REGGAE | RAP | SKA | CROSSOVER <br></h5>
        <div class="qt-social">
            <a href="https://itunes.apple.com/de/artist/shanti-powa/id586835713"><span class="qticon-itunes"></span></a>
            <a href="https://www.facebook.com/ShantiPowa/"><span class="qticon-facebook"></span></a>
            <a href="https://twitter.com/shantipowa/"><span class="qticon-twitter"></span></a>
            <a href="https://www.youtube.com/shantipowa"><span class="qticon-youtube"></span></a>
            <a href="https://soundcloud.com/shantipowa"><span class="qticon-soundcloud"></span></a>
            <a href="https://www.instagram.com/shantipowamusic/"><span class="qticon-instagram"></span></a>
            <a href="https://bit.ly/shantipowaspotify"><span class="qticon-qticons-spotify"></span></a>
            <br>
            <br><br><br><br><br><br>
            <h5><a href="https://www.instagram.com/sirgulliver.art/">Designed & Curated by sirgulliver.art</a></h5>
        </div>
    </div>
    <div class="qt-particles" id="particlesfooter" data-color="#00FFB0" data-opacity="0.2" data-speed="1"></div>
</footer>
<div class="qt-firefoxfix"></div>

