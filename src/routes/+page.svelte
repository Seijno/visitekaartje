<script>
	import Music from './MusicCard.svelte';
    import LinkedIn from './LinkedIn.svelte';
    import Socials from './SocialCard.svelte';
    
    let originalBottomValues = [2, 3.5, 5];
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
     <main>
        <div class="coverup"></div>
        <div style="bottom: {bottomValues[0]}rem; background: red; z-index: 3; "><Music></Music></div>
        <div style="bottom: {bottomValues[1]}rem; background: blue; z-index: 2; "><LinkedIn></LinkedIn></div>
        <div style="bottom: {bottomValues[2]}rem; background: green; z-index: 1; "><Socials></Socials></div>
        <button on:click={updateBottomValues}>
        </button>
     </main>
</body>

<style>
    body{
        background: rgb(215, 207, 207);
        margin: 0;
        padding: 0;
    }
    main{
        background: rgb(37, 37, 37);
        position: absolute;
        bottom: 0;
        left: 40%;
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
        transition: 0.4s;
    }
    div{
        position: absolute;
        margin-right: 2rem;
        border-radius: 15px;
        width: 20rem;
        height: 16rem;
        rotate: 90deg;
        z-index: 1;
        transition: .5s;  
    }
    .coverup{
        position: absolute;
        background: rgb(37, 37, 37);
        width: 19rem;
        height: 22rem;
        bottom: 0rem;
        rotate: 0deg;
        padding-bottom: 3rem;
        z-index: 4;
    }
</style>