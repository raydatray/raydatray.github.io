<script>
    import Project from './project.svelte';
    import "../app.css";

    import {IconBrandLinkedin, IconBrandGithub, IconMail, IconDownload, IconBrandRust, IconBrandSvelte, IconCoffee, IconBrandCarbon, IconBrandPython, IconBrandTypescript} from '@tabler/icons-svelte'

    const projectOne = {
        projectName: "AssetPlus",
        shortHeader: "Java powered hotel asset management app",
        description: "",
        date: "November 2023",
        link: "ooga booga",
        imageURL: "url here...."
    }

    const projectTwo = {
        projectName: "PyroBot3",
        shortHeader: "Python powered lego fire extinguishing robot",
        date: "November 2023",
        link: "ooga booga",
        imageURL: "src/static/images/PyroBot3.png"
    }

    const projectThree = {
        projectName: "RustyChip8",
        shortHeader: "Cross platform Chip8 emulator built in Rust",
        date: "",
        link: "ooga booga",
        imageURL: "url here..."
    }

    const projectFour = {
        projectName: "Othello ",
        shortHeader: "Othello with  (Also my first foray into programming!)",
        date: "May 2022",
        link: "ooga booga",
        imageURL: "url here..."
    }
</script>
<div class = 'flex flex-col items-center'>

<div class = 'container'>
    <div class = 'header'>
        <h1>Ray Liu</h1>
        <p> My picture will be here one day</p>
    </div>

    <div class = 'buffer'></div>

    <div class = 'links'>
        <p class = 'text-right'>I break things, lots of things</p>
        <br/>
        <div class = 'grid grid-flow-col auto-cols-max justify-end'>
            <a href = 'https://www.linkedin.com/in/raydatray/'>
                <IconBrandLinkedin size = {36}/>
            </a>
            <a href = 'https://github.com/raydatray'>
                <IconBrandGithub size = {36}/>
            </a>
            <a href = 'raydatray@gmail.com'>
                <IconMail size = {36}/>
            </a>
        </div>
    </div>

    <div class = 'work'>
        <h2>Experience</h2>

        <span>May 2023 - August 2023</span>

        <p>Intern in Technology and Innovation @ <span>Will Solutions</span>, where I created internal development tools in TypeScript </p>

        <br/>
        <p>Looking for a <span>Summer 2024</span> internship</p>

        <br/>
        
        <a href = 'src/static/file/2024_Internship_Resume V3.pdf'>
            <div class = "grid grid-flow-col auto-cols-max gap-3 justify-start">
                <IconDownload/>
                <p>Download resume</p>
            </div>
        </a>

        
    </div>

    <div class = 'education'>
        <h2>Eduation</h2>
        <p>U2 BEng Software Engineering @ <span>McGill University</span>, expecting to graduate in <span>May 2026</span>.</p>
        <br/>
        <p>Health Sciences @ <span>Marianopolis College</span>, graduated in May 2022 with an Rscore of <span>34.9</span>.</p>
    </div>

    <div class = 'about'>
        <h2>Tidbits</h2>

        <b>My Toolbox</b>
        <div class = 'grid grid-flow-col auto-cols-max justify-start'>
            <IconBrandRust size = {36} stroke = {1.5}/>
            <IconBrandSvelte size = {36} stroke = {1.5}/>
            <IconCoffee size = {36} stroke = {1.5}/>
            <IconBrandCarbon size = {36} stroke = {1.5}/>
            <IconBrandPython size = {36} stroke = {1.5}/>
            <IconBrandTypescript size = {36} stroke = {1.5}/>
        </div>

        <br/>

        <b>Some of my hobbies</b>

    </div>

    <div class = 'projects'>
        <h2>Projects</h2>
        <p>Some of the things I've worked on</p>

        <Project {...projectOne} />

        <Project {...projectTwo} />

        <Project {...projectThree} />

        <Project {...projectFour} />

    </div>
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
        width: 95vw;          
        margin-top: 3em;
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

    .buffer {
        border-right: none;
        border-left: none;
    }

    .header {
        border-right: none;
    }

    .links {
        border-left: none;
    }

</style>
