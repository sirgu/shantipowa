<script>
// @ts-nocheck

export let bio;
</script>

<div id="bio" class="section section-bio parallax-container qt-fullscreen scrollspy" >
    <div class="parallax" ><img src="images/SP_rOLLINGoN_WEB_03_BG.png" alt="background"></div>
    <div class="container">
        <div class="qt-framed flow-text"  data-100p-top="opacity:0;" data-80p-top="opacity:0;" data-30p-top="opacity:1;" >
            <h2 class="qt-section-title">DATES &amp; BIO<i class="deco"></i></h2>
            <div class="content qt-polydecor poly2">
                <h4>
                    {#if bio}
                    {@html bio[0].dates.replaceAll('\r\n','<br>').replace('\"','"')}
                    <br>
                    {/if}
                </h4>

        <h4>Info & Booking: info@shantipowa.com <br>
        We are working on getting concerts on the track again<br>
        Tour organised in collaboration with Galo Bookings <br><br></h4>

        <h4>BIO<br><br></h4>
        <h5>
            
        {#if bio}
            {@html bio[0].bio.replaceAll('\r\n','<br>').replace('\"','"')}
            <br>
        {/if}





            <!--Shanti Powa Orchestra is a big band from northern Italy founded in 2010. They produce a very powerful Crossover of Reggae, Dub, Rap, Ska, Dancehall, Funk &amp; Rock. Because of the different cultural backgrounds of the band members, the lyrics are written in English, Italian, French and German.

On stage Shanti Powa are full of energy; and that combined with their innovative music creates a very unique atmosphere involving the whole crowd. In their career Shanti Powa Orchestra have already played hundreds of shows all over Europe (Rototom Sunsplash (ES), Overjam (SL), Boomtown (UK), Sunrise (DE), Reeds (CH)...) sharing the stage with artists such as Alborosie, Toots & The Maytals, Max Romeo, The Gladiators, Israel Vibrations, Dub Fx, Julian Marley, Mellow Mood, Luciano, Shaggy, Inner Circle & many more.

In 2014 the band released their first album "The Orchestra", followed up by "Peaceful Warriors" in 2016. In 2018 they released their third album "'Til Insanity" All three albums have been produced by Shanti Powa and released through their own independent label "Shanti Powa Records".
-->
        </h5>
        </div>
        </div>
    </div>
</div>