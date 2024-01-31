<script>
    import Project from './project.svelte'
    import "../app.css"

    const projectOne = {
        projectName: "AssetPlus",
        description: "ooga booga",
        date: "November 2023",
        link: "ooga booga",
        imageURL: "url here...."
    }

    const projectTwo = {
        projectName: ""
    }

    const projectThree = {

    }
</script>

<div class = 'container'>
    <div class = 'header'>
        <h1>Ray Liu</h1>
        <p> My picture will be here one day</p>
    </div>

    <div class = 'buffer'></div>

    <div class = 'links'>
        <p>placeholder</p>
    </div>

    <div class = 'work'>
        <h2>Experience</h2>

        <span>May 2023 - August 2023</span>

        <p>Intern in Technology and Innovation @ <span>Will Solutions</span>, where I worked on  </p>

        <br/>
        <p>Looking for a <span>Summer 2024</span> internship</p>

        <br/>
    </div>

    <div class = 'education'>
        <h2>Eduation</h2>
        <p>U2 BEng Software Engineering @ <span>McGill University</span>, expecting to graduate in <span>May 2026</span>.</p>
        <br/>
        <p>Health Sciences @ <span>Marianopolis College</span>, graduated in May 2022 with an Rscore of <span>34.9</span>.</p>
    </div>

    <div class = 'about'>
        <h2>Tidbits</h2>
        <b></b>


        <b>Some of hobbies</b>
    </div>

    <div class = 'projects'>
        <h2>Projects</h2>
        <p>Some of projects I've worked on</p>

        <br/>

        <Project {...projectOne} />

    </div>
</div>

<style lang="postcss">
    .container {
        display: grid;
        grid-template-areas:
            'header buffer links'
            'work projects projects'
            'education projects projects'
            'about projects projects';
        grid-template-columns: 1.5fr 1fr 2fr;
        grid-template-rows: auto auto auto 1fr;
        background-color: white;
        border: 3px solid black;               
        margin: 3em;
        z-index: 1;
    }

    .header, .buffer, .links, .work, .education, .projects, .about {
        padding: 2em;
        background-color: white;
        border: 1px solid black
    }

    .projects{
        grid-area: projects
    
    }


</style>
