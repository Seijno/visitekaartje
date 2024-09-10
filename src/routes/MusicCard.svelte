<script>
    import spotify from '$lib/assets/Spotify_Primary_Logo_RGB_Green.png'
    import stringent from '$lib/assets/Schermafbeelding 2024-09-10 223329.png'
</script>
<article>
    <img class="spotifyLogo" src={spotify} alt="spotify logo">
    <img class="bandpic" src={stringent} alt="spotify profile of the band Stringent.">
    <div>
        <ul>
            <p>Released songs:</p>
            <li>Say My Name</li>
        </ul>
        <ul>
            <p>Upcoming album tracks:</p>
            <li>Army of the dead</li>
            <li>Pushing through</li>
            <li>more</li>
        </ul>
    </div>
</article>

<style>
.spotifyLogo{
    width: 2.5rem;
    rotate: -90deg;
}
.bandpic{
    width: 100%;
    height: 100%;
}
div{
    border-radius: 5px 5px 15px 15px;
    /* border: #1ed760 solid .5rem; */
    display: flex;
    color: black;
    background: #1ed760;
    padding-bottom: 1.3rem;
}
ul{
    display: flex;
    flex-direction: column;
    font-size: 11px;
}
p {
    font-size: 11px;
}
</style>
