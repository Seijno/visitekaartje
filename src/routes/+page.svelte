<script>
	import Music from './MusicCard.svelte';
    import LinkedIn from './LinkedIn.svelte';
    import Socials from './SocialCard.svelte';
    
    let originalBottomValues = [2.5, 5, 7.5];
    let bottomValues = [...originalBottomValues];
    let isToggled = false;


    function updateBottomValues() {
        if(!isToggled){
            bottomValues = bottomValues.map(value => value + 7);
        } else {
            bottomValues = [...originalBottomValues];
        }
        isToggled = !isToggled;
    }
</script>
<body>
    <h1>The cardholder!</h1>
     <main>
        <a href="https://linktr.ee/seijnovannieuwkoop"><div class="cart" style="bottom: {bottomValues[2]}rem; background: rgb(255,222,98); background: linear-gradient(117deg, rgba(255,222,98,1) 25%, rgba(0,243,240,1) 100%); "><Socials></Socials></div></a>
        <a href="https://www.linkedin.com/in/seijno-van-nieuwkoop-17852020a/"><div class="cart" style="bottom: {bottomValues[1]}rem; background: #0066c8; "><LinkedIn></LinkedIn></div></a>
        <a href="https://open.spotify.com/artist/7jUFx2NIq6vFbcfJptuKlU"><div class="cart" style="bottom: {bottomValues[0]}rem; background: black;"><Music></Music></div></a>
        <div class="coverup"></div>
        <button on:click={updateBottomValues}>
        </button>
     </main>
</body>

<style>
    body{
        position: relative;
        background: rgb(248,0,255);
        background: linear-gradient(153deg, rgba(248,0,255,1) 0%, rgba(0,243,240,1) 100%);
        margin: 0;
        padding: 0;
        height: 100vh;
        overflow: hidden;
    }
    main{
        background: rgb(37, 37, 37);
        position: absolute;
        margin: 0 auto;
        top: 50%;
        left: 38%;
        transform: translateY(-30%);
        width: 20rem;
        height: 25rem;
        border: 1px solid black;
        border-radius: 15px;
        z-index: 4;
    }
    button{
        background: rgb(106, 106, 106);
        position: absolute;
        border-radius: 15px 15px 0 0;
        left: 17rem;
        bottom: 16rem;
        width: 8rem;
        height: 3rem;
        margin: 0;
        transition: 0.8s;
        rotate: 90deg;
    }
    button:hover{
        bottom: 15.5rem;
        transition: 0.4s ease;
        cursor: pointer;
    }
    .cart{
        position: absolute;
        border-radius: 15px;
        width: 20rem;
        height: 16rem;
        rotate: 90deg;
        transition: .5s ease;
        cursor: pointer; 
    }
    .coverup{
        position: absolute;
        background: rgb(37, 37, 37);
        width: 18rem;
        height: 22rem;
        bottom: 0rem;
        rotate: 0deg;
        padding-bottom: 3rem;
        margin-left: 1rem;
        z-index: 3;
        cursor: auto;
    }
    .cart:hover{
        rotate: 0deg;
        scale: 1.5;
        transition: .8s;
        z-index: 4;
    }
    h1{
        text-align: center;
        width: 100%;
    }
    @media screen and (max-width: 700px) {
        main {
        left: 17%;
    }
}
</style>