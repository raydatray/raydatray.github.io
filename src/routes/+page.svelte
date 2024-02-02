<script>
    import Project from './project.svelte';
    import "../app.css";

    import {IconBrandLinkedin, IconBrandGithub, IconMail, IconDownload, IconBrandRust, IconBrandSvelte, IconCoffee, IconBrandCarbon, IconBrandPython, IconBrandTypescript} from '@tabler/icons-svelte'

    const assetPlus = {
        projectName: "AssetPlus",
        shortHeader: "Java powered hotel asset management app",
        description: "",
        date: "November 2023",
        link: "https://github.com/raydatray/AssetPlus",
        imageURL: "/AssetPlus.png"
    }

    const pyroBot3 = {
        projectName: "PyroBot3",
        shortHeader: "Python powered lego fire extinguishing robot",
        description: "",
        date: "November 2023",
        link: "https://github.com/raydatray/BrickPy3Driver",
        imageURL: "/PyroBot3.png"
    }

    const projectThree = {
        projectName: "RustyChip8",
        shortHeader: "Cross platform Chip8 emulator built in Rust, compiled to Wasm", 
        date: "Ongoing",
        link: "",
        imageURL: ""
    }

    const Reversi = {
        projectName: "Othello ",
        shortHeader: "Othello with various AI players, and a quantitative performance analysis of them (Also my first foray into programming!)",
        description: "",
        date: "May 2022",
        link: "https://github.com/raydatray/Reversi",
        imageURL: "/Reversi.png"
    }
</script>
<div class = 'flex flex-col'>
    <div class = 'flex flex-col items-center'>

        <div class = 'container'>
            <div class = 'header'>
                <h1>Ray Liu</h1>
                <p> A picture will be here one day</p>
            </div>

            <div class = 'buffer'></div>

            <div class = 'links flex flex-col items-end justify-between h-full'>
                <div>
                    <p class = 'text-right font-semibold'>I break things, lots of things</p>
                    <div class = 'grid grid-flow-col auto-cols-max gap-1 justify-end'>
                        <a href = 'https://www.linkedin.com/in/raydatray/'>
                            <IconBrandLinkedin size = {36} stroke = {1.5}/>
                        </a>
                        <a href = 'https://github.com/raydatray'>
                            <IconBrandGithub size = {36} stroke = {1.5}/>
                        </a>
                        <a href= 'mailto: raydatray@gmail.com'>
                            <IconMail size = {36} stroke = {1.5}/>
                        </a>
                    </div>
                </div>

                <p class = "inline-block align-bottom text-right text-xs align-bottom">Built with<span>❤️</span>using <span class = "text-xs">Svelte</span></p>
            </div>

            <div class = 'work'>
                <h2>Experience</h2>

                <span>May 2023 - August 2023</span>

                <p>Intern in Technology and Innovation @ <span>Will Solutions</span>, where I created internal development tools in TypeScript </p>

                <br/>
                <p>Looking for a <span>Summer 2024</span> internship</p>

                <br/>
                
                <a href = "/Resume.pdf">
                    <div class = "grid grid-flow-col auto-cols-max gap-3 justify-start">
                        <IconDownload/>
                        <span>Download resume</span>
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
                <h2>Questions? Answers!</h2>
                <b>Your location?</b>
                <p>Currently in Montreal, Canada. From Ottawa.</p>
                <br/>

                <b>Your Tools?</b>
                <div class = 'grid grid-flow-col auto-cols-max gap-0.5 justify-start'>
                    <IconBrandRust size = {36} stroke = {1.5}/>
                    <IconBrandSvelte size = {36} stroke = {1.5}/>
                    <IconCoffee size = {36} stroke = {1.5}/>
                    <IconBrandCarbon size = {36} stroke = {1.5}/>
                    <IconBrandPython size = {36} stroke = {1.5}/>
                    <IconBrandTypescript size = {36} stroke = {1.5}/>
                </div>
                <br/>

                <b>Your goals in Tech? </b>
                <p>I am looking to experience as many domains </p>
                <br/>

                <b></b>

                <b>Any hobbies?</b>
                <ul>
                    <li>- Occasional weightlifter</li>
                    <li>- "Decent" at cooking</li>
                    <li>- All things computers (custom loops, keyboards, everything)</li>
                    <li>- Serial tinkerer (and electronics frier)</li>
                </ul>

            </div>

            <div class = 'projects'>
                <h2>Projects</h2>
                <p>Some of the things I've worked on</p>
                <br/>

                <Project {...assetPlus} />

                <Project {...pyroBot3} />

                <Project {...projectThree} />

                <Project {...Reversi} />

            </div>
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
        grid-template-columns: 1.25fr 1fr 2fr;
        grid-template-rows: auto auto auto 1fr;
        background-color: white;
        border: 3px solid black;  
        width: 95vw;          
        margin-top: 3em;
        margin-bottom: 3em;
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
