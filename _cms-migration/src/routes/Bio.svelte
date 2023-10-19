<script>
	import { onMount } from "svelte";


// @ts-nocheck

onMount(() => {
    (function($) {
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

        $.fn.parallaxPolydecor();
        
    })(jQuery);
});

export let bio;
</script>

<div id="bio" class="section section-bio parallax-container qt-fullscreen scrollspy" >
    <div class="parallax" ><img src="img/SP_rOLLINGoN_WEB_03_BG.webp" alt="background"></div>
    <div class="container">
        <div class="qt-framed flow-text"  data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-30p-top="opacity:1;" >
            <h2 class="qt-section-title">DATES &amp; BIO<i class="deco"></i></h2>
            <div class="content qt-polydecor poly2">
                <h4>
                    {#if bio && bio[0].dates}
                    {@html bio[0].dates.replaceAll('\r\n','<br>').replace('\"','"')}
                    <br>
                    <br>
                    {/if}
                </h4>


                <h4>BIO<br><br></h4>
                <h5>  
                {#if bio}
                    {@html bio[0].bio.replaceAll('\r\n','<br>').replace('\"','"')}
                    <br>
                    <br>
                {/if}
                </h5>
            </div>
        </div>
    </div>
</div>