<script>
    import linkedIn from "$lib/assets/linkedin-logo-linkedin-icon-transparent-free-png.png"
    import profile from "$lib/assets/Schermafbeelding-linkedin.png"
</script>
<img class="logo" src={linkedIn} alt="linkedIn logo">
<img class="linked" src={profile} alt="linkedin profiel">
<div>
    <ul>
        <p>Education</p>
        <li>Mbo Rijnland - Software Developer</li>
        <li>HVA - Frontend design & programming</li>
    </ul>
    <ul>
        <p>Work experience</p>
        <li>Jumbo all rounder</li>
    </ul>
</div>
<style>
.logo{
    width: 2.5rem;
    rotate: -90deg;
}
.linked{
    width: 100%;
}
div{
    border-radius: 5px 5px 15px 15px;
    display: flex;
    color: black;
    background: #4399ea;
}
ul{
    display: flex;
    flex-direction: column;
    font-size: 11px;
    padding-right: 1rem;
}
p {
    font-size: 11px;
}
</style>