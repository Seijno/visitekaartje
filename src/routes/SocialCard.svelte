<script>
    import linkedIn from "$lib/assets/linkedin-logo-linkedin-icon-transparent-free-png.png"
    import insta from "$lib/assets/Instagram_logo_2016.png"
    import github from "$lib/assets/githubLogo.png"
    import spotify from '$lib/assets/Spotify_Primary_Logo_RGB_Green.png'
    import gmail from "$lib/assets/Gmail_Logo.png"
</script>
<img class="cardLogo" src={insta} alt="instagram logo">
<div>
    <div class="socialItem">
        <img class="socialLogo" src={insta} alt="instagram logo">
        <p>@Seijnovannieuwkoop</p>
    </div>
    <div class="socialItem">
        <img class="socialLogo" src={github} alt="github logo">
        <p class="center">@Seijno</p>
    </div>
    <div class="socialItem">
        <img class="socialLogo" src={linkedIn} alt="linkedIn logo">
        <p>Seijno Van Nieuwkoop</p>
    </div>
    <div class="socialItem">
        <img class="socialLogo" src={spotify} alt="spotify logo">
        <p class="center">@Stringent</p>
    </div>
    <div class="gmailItem">
        <img class="socialLogo" src={gmail} alt="gmail logo">
        <p>seijnovannieuwkoop@gmail.com</p>
    </div>
</div>
<style>
    .cardLogo{
        width: 2rem;
        rotate: -90deg;
    }
    div{
        display: flex;
        flex-wrap: wrap;
    }
    .socialItem{
        flex-direction: row;
        width: 45%;
        height: 30%;
        background: rgb(255, 255, 255);
        border-radius: 5px;
        margin: 1rem 0 0 0.5rem;
        line-height: 1.5rem;
        text-align: center;
    }
    .gmailItem{
        flex-direction: row;
        width: 80%;
        height: 30%;
        background: rgb(255, 255, 255);
        border-radius: 5px;
        margin: 1rem 3rem;
    }
    .socialLogo{
        width: 3rem;
    }
    p{
        font-size: 10px;
        color: black;
    }
    .center{
        width: 50%;
    }
    
</style>