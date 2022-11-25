<script>
// @ts-nocheck

import { onMount } from "svelte";
export let photos;

onMount(()=>{
    (function($){
        $('.qtgallery').slick({
            slidesToScroll: 1,
            slidesToShow: 1,
            infinite: true,
            dots: true,
            variableWidth: true,
            arrows: true,
            centerMode: true,
            // centerPadding: '140px',
            responsive: [
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
        $('.qtgallery').slick('slickGoTo', 0);
    })(jQuery);
    
});
</script>
<div id="photos" class="section section-photos black scrollspy">
    <h2 class="qt-section-title" data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-50p-top="opacity:1;">PHOTOS<i class="deco"></i></h2>
    <div class="qtgallery"  data-bottom-top="opacity:0;" data-center-top="opacity:1;">
        {#if photos}
        {#each photos as photo}
            <div><img src="{photo.img.path}" alt="{photo.title}"></div>
        {/each}
        {/if}

            
    </div>
</div>