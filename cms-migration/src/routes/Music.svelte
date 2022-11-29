<script>
// @ts-nocheck

import { onMount } from "svelte";
export let music;
let type = 'soundcloud';
let src = '';


function openIframe(typ, link){
    type = typ;
    src = link;
}

onMount(() => {
    (function($){
        $.fn.gridstackCarousel = function(){
            $('.qt-gridstackCarousel').each(function(i,c){
                var that = $(c),
                    w = that.width(),
                    h = w/16*7,
                    QTtime_constant = that.attr("data-time_constant"),
                    QTdist = that.attr("data-dist"),
                    QTshift = that.attr("data-shift"),
                    QTvpadding = that.attr("data-vpadding"),
                    QTfull_width = (that.attr("data-full_width") === "1" || that.attr("data-full_width") === "true"),
                    QTpadding = that.attr("data-padding");
                if(QTtime_constant == undefined || QTtime_constant === "" ) {
                    QTtime_constant = 200;
                }
                if(QTdist == undefined || QTdist === "" ) {
                    QTdist = -30;
                }
                if(QTshift == undefined || QTshift === "" ) {
                    QTshift = 0;
                }
                if(QTpadding == undefined || QTpadding === "" ) {
                    QTpadding = 0;
                }
                if(QTvpadding == undefined || QTvpadding === "" ) {
                    QTvpadding = 0;
                }
                if(QTvpadding !== 0){
                    that.css({"margin-top":QTvpadding,"margin-bottom":QTvpadding});
                } 
                var atts = {
                    time_constant: parseInt(QTtime_constant, 10),
                    dist: parseInt(QTdist, 10),
                    padding: parseInt(QTpadding, 10),
                    shift:parseInt(QTshift, 10),
                    full_width: QTfull_width
                };
                that.carousel(atts);


                that.parent().find(".prev").on("click",function(e){
                    e.preventDefault();
                    that.carousel("prev");
                });
                that.parent().find(".next").on("click",function(e){
                    e.preventDefault();
                    that.carousel("next");
                });
                that.find(".carousel-item").on("mouseenter touchstart", function(e){
                    var itemElem = $(this);
                    itemElem.addClass("active");
                    if($("body").hasClass("mobile")){
                        setTimeout(
                        function(){ 
                            itemElem.removeClass("active"); 
                        } ,  3000);
                        that.find("a").on("touchstart", function(e){
                            window.location.href = $(this).attr("href");
                        });
                    }
                }).on("mouseleave", function(){
                    $(this).removeClass("active");
                });
            });
        }
        // $(".modal-trigger").on("click",function(e){
        //     e.preventDefault();
        //     if($(this).attr("data-iframe") !== undefined) {
        //         $("#modalframe").attr("src", $(this).attr("data-iframe"));
        //     }
        //     return true;
        // });

        //  initialize the modal window of the album
        $('.modal-trigger').leanModal();

        $.fn.gridstackCarousel();
    })(jQuery);
});
</script>

<div id="music" class="section section-music parallax-container scrollspy" >
    <div class="parallax"><img src="img/parallax3.webp" alt="background">
    </div>
    <h2 class="qt-section-title" data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-50p-top="opacity:1;" data-30p-top="opacity:1;" data-8p-top="opacity:1;" data-0p-top="opacity:0;">MUSIC<i class="deco"></i></h2>
    <div id="carouselmusic" class="qt-gridstackCarousel-container">
        <div class="carousel qt-gridstackCarousel" data-vpadding="50" data-time_constant="500"   data-dist="-30"  data-shift="-20" data-padding="20" data-full_width="0" data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-50p-top="opacity:1;" data-30p-top="opacity:1;" data-top-bottom="opacity:0;">
            {#if music}
            {#each music as song}

            <div class="carousel-item">
                <img src="{song.img.path}"  width="300" height="300" alt="{song.title}">
                <h5>{song.title}</h5>
                <a href="#modal1" class="btn modal-trigger" on:click={openIframe(song.source, song.link)}><span class="lnr lnr-music-note"></span></a>
            </div>
            {/each}
            {/if}
        </div>
        <div class="nav hide-on-med-and-down">
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="prev">
                <span class="lnr lnr-arrow-left-circle"></span>
            </a>
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="next">
                <span class="lnr lnr-arrow-right-circle"></span>
            </a>
        </div>
    </div>
</div>

<div id="modal1" class="modal bottom-sheet">
    <div class="modal-content">
        <!-- <iframe ></iframe> -->
        <iframe title="soundcloud" id="modalframe" class="qt-modalframe" {src} style={type === 'spotify' ? "border-radius:12px" : ''}></iframe>
    </div>
</div>
