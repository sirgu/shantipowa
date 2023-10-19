<script>
// @ts-nocheck

import { onMount } from "svelte";

export let videos;

onMount(()=>{
    (function($){
        $('.qtvideos').slick({
            centerMode: true,
            centerPadding: '120px',
            slidesToShow: 2,
            responsive: [
                {
                breakpoint: 768,
                settings: {
                    arrows: false,
                    centerMode: false,
                    slidesToShow: 2
                }
                },
                {
                breakpoint: 480,
                settings: {
                        arrows: true,
                        centerMode: false,
                        // centerPadding: '40px',
                        variableWidth: false,
                        variableHeight: false,
                        slidesToShow: 1,
                        draggable: true,
                        swipe: true,
                        touchMove: true
                    }
                }
            ]
            });
    })(jQuery);
});
</script>

<div id="video" class="section section-video  scrollspy" >
    <div class="qt-framed flow-text"  data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-30p-top="opacity:1;" >
        <h2 class="qt-section-title">VIDEOS<i class="deco"></i></h2>
        <div class="content">
            <div class="qtvideos">
                {#if videos}
                {#each videos as video}
                    {#if video.public && video.img && video.img.path && video.title && video.link}
                    <div><a href="{video.link}" frameborder="0" allowfullscreen> <img src="{video.img.path}" alt="video"><span class="lnr lnr-film-play"></span></a><h5>{video.title}</h5></div>
                    {/if}
                {/each}
                {/if}
            </div>
        </div>
    </div>
</div>