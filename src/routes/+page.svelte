<script>
    import { onMount } from 'svelte';

    import Nav from "./Nav.svelte";
    import Theme from "./Theme.svelte"
    import Section from "./Section.svelte";
    import Contact from "./Contact.svelte";
    import ProgramTable from "./ProgramTable.svelte";
    import ProgramTableEntry from "./ProgramTableEntry.svelte";
    import Speaker from "./Speaker.svelte";

    onMount(() => {
        // Check if there is a hash in the URL
        if (window.location.hash) {
            const element = document.querySelector(window.location.hash);
            if (element) {
                const offset = 50; // Adjust this offset as needed
                const elementPosition = element.getBoundingClientRect().top + window.pageYOffset;

                // Scroll to the adjusted position with optional smooth scrolling
                window.scrollTo({
                    top: elementPosition - offset,
                    behavior: 'smooth' // Optional: change to 'auto' for instant scroll
                });
            }
        }
    });

</script>

<div class="min-h-full">
    <Nav 
        home={{name: "IEEE ITSC 2024", href: "https://ieee-itsc.org/2024"}} 
        sections={[
            {name: "Small-Scale CAVs", href: "#small-scale"},
            {name: "Smart Mobility", href: "#smart-mobility"},
        ]}/>
    
    <Theme 
        id="small-scale"
        title="Small-Scale Testbeds for Connected and Automated Vehicles in Research and Education"
        subtitle="at IEEE ITSC 2024"
        date="September 24, 2024"
        room="Salon 19/20">

        <Section title="Abstract">
            <div class="overflow-hidden">
                <div class="aspect-square w-full pb-4 sm:float-right sm:w-1/2 sm:pl-4 lg    :w-1/3 lg:pl-6 lg:pb-6">
                    <img class="object-cover rounded shadow" src="svea.jpeg" alt="Small-Scale vehicle under testing">
                </div>
                <p class="text-justify pb-3">The growing importance of Connected and Automated Vehicles (CAVs) calls for innovative platforms to develop, test, and validate new algorithms and technologies. Small-scale testbeds offer an effective means to prototype and experiment with close to real-world conditions. Furthermore, these platforms tend to be powerful research demonstrators that motivate collaborations within and outside academia. However, these testbeds present unique challenges in terms of accessibility, reproducibility, and integration into educational frameworks. To better approach these challenges, this workshop aims to facilitate discussions on learnings and best practices. In particular, the workshop focuses on addressing these issues with an emphasis on leveraging small-scale testbeds for research and education.</p>
            </div>
        </Section>
        
        <Section title="Program">
            <div class="overflow-x-auto">
                <ProgramTable>
                    <ProgramTableEntry time="08:30 - 08:50">
                        <p>Arrival and Registration</p>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="08:50 - 09:00" vertical={false}>
                        <p>Opening Remarks</p>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="09:00 - 09:30">
                        <Speaker
                            name="Andreas Malikopoulos" affiliation="Cornell University"
                            title="A Research and Educational Scaled, Smart City Testbed for Real-Time Control of Autonomous Driving Systems"
                            />
                    </ProgramTableEntry>
                    
                    <ProgramTableEntry time="09:30 - 10:00">
                        <Speaker
                            name="Simon Schäfer" affiliation="RWTH Aachen University"
                            title="Cyber-Physical Mobility Lab: An Open-Source Testbed for Connected and Automated Vehicles"
                            abstract="This talk will present our Cyber-Physical Mobility Lab (CPM Lab), an open-source, remotely accessible platform for Connected and Automated Vehicles (CAVs) focusing on multi-agent decision-making. The CPM Lab provides a deterministic computation model that allows for reproducible experiments. Using its digital twin, it can seamlessly extend its 20 small-scale vehicles (µCars) with virtual µCars. We created a research and teaching stack around the CPM Lab: undergraduate students study programming in the CPM Academy, graduate students study coordination and control of CAVs, and researchers compete in the CPM Olympics. The CPM Lab is one of the pioneering testbeds for CAVs and has been rebuilt at other universities, establishing its influence in academic settings."/>
                    </ProgramTableEntry>
                    
                    <ProgramTableEntry time="10:00 - 10:30" vertical={false}>
                        <p>Coffee Break</p>
                    </ProgramTableEntry>
                    
                    <ProgramTableEntry time="10:30 - 11:00">
                        <Speaker
                            name="Simon Thompson" affiliation="TIER IV"
                            title="Autoware Reference Platforms: From Small Scale to Full Scale Autonomous Vehicles"
                            />
                    </ProgramTableEntry>
                    
                    <ProgramTableEntry time="11:00 - 11:30">
                        <Speaker
                            name="Kaj Munhoz Arfvidsson" affiliation="KTH Royal Institute of Technology"
                            title="SVEA and Recent Experiences With Small-Scale Vehicles in Industrial Collaborations"
                            abstract="As the demand for Connected and Automated Vehicles (CAVs) continues to rise, scalable, cost-effective platforms like small-scale testbeds are becoming increasingly crucial for prototyping, testing, and refining CAV technologies. This talk will present the SVEA platform, an open-source, small-scale testbed designed for evaluating novel automation techniques and V2X use-cases. Drawing from real-world experiences, the presentation will highlight how the SVEA platform has been used in recent experiments with industrial partners. In addition, the platform has served as an educational platform for teaching automatic control. With these experiences, the talk will cover how to lead collaborative industrial projects, opportunities for innovation, and pathways for future industry-academic partnerships while using the platform in education."/>
                    </ProgramTableEntry>
                    
                    <ProgramTableEntry time="11:30 - 12:15" vertical={false}>
                        <p><b>Panel Discussion</b></p>
                        <p>Moderated by Jonas Mårtensson</p>
                    </ProgramTableEntry>
                </ProgramTable>
            </div>
        </Section>
        
        <Section title="Organizers">
            <div class="flex flex-col md:flex-row items-start md:items-center justify-evenly space-y-4 md:space-y-0 md:space-x-8 px-4 mx-auto">
                <Contact
                    name="Kaj Munhoz Arfvidsson"
                    affiliation="KTH Royal Institute of Technology"
                    email="kajarf@kth.se"
                    image="https://www.kth.se/files/avatar/kajarf"/>
                <Contact
                    name="Jonas Mårtensson"
                    affiliation="KTH Royal Institute of Technology"
                    email="jonas1@kth.se"
                    image="https://www.kth.se/files/avatar/jonas1"/>
            </div>
        </Section>

    </Theme>

    <Theme
        id="smart-mobility"
        title="Smart Mobility: AI and Intelligent Decision-Making for Future Transportation Systems"
        subtitle="at IEEE ITSC 2024"
        date="September 24, 2024"
        room="Salon 19/20">

        <Section title="Abstract">
            <div class="overflow-hidden">
                <div class="aspect-square w-full pb-4 sm:float-right sm:w-1/2 sm:pl-4 lg    :w-1/3 lg:pl-6 lg:pb-6">
                    <img class="object-cover rounded shadow" src="smart-mobility.jpg" alt="Futuristic city with AI-connected roads">
                </div>
                <p class="text-justify pb-3">The workshop focuses on the transformative potential of artificial intelligence and advanced decision-making technologies in modern transportation. As urban environments evolve and demand smarter mobility solutions, this workshop will explore how AI, data analytics, and intelligent systems can enhance traffic management, road safety, and autonomous driving.</p>
                <p class="text-justify pb-3">Through a series of expert-led discussions, the workshop will cover topics such as leveraging real-world vehicle data, the development of digital twins for transportation modeling, the integration of reinforcement learning with planning and control systems, and ensuring robustness and trust in AI explanations for autonomous vehicles. Participants will gain insights into the latest advancements in smart mobility, offering a forward-looking view on the future of transportation systems.</p>
            </div>
        </Section>
        
        <Section title="Program">
            <div class="overflow-x-auto">
                <ProgramTable>
                    <ProgramTableEntry time="13:30 - 13:35" vertical={false}>
                        <p>Opening Remarks</p>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="13:35 - 14:30">
                        <Speaker
                            name="David Goldstein and Lavanya Sayam" affiliation="IEEE National Transportation Data & Analytics Solutions"
                            title="IEEE NTDAS: Driving global roadways research with real-world vehicle data analytics platform"
                            abstract="IEEE's National Transportation Data and Analytics Solution is a powerful platform that provides a unique, robust, and high-quality transportation dataset combined with advanced analytics tools, enabling valuable insights to empower academic research and instruction. Equipped with 5 min granularity data for speed and travel time, for both trucks and passenger vehicles, the NTDAS supports a multitude of use cases across domains whether it be in logistics / supply chain, freight research, urban studies and planning, sustainability, equity, safety, environment, urban and rural dynamics, and many others. This session speaks to the impactful ways NTDAS can be incorporated into research and teaching, with specific use case examples relevant to the global audience."/>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="14:30 - 15:00">
                        <Speaker
                            name="Yunchen Ge and Marcelo Contreras Cabrera" affiliation="University of Alberta"
                            title="Development a Digital Twin Visualizer for Intelligent Transportation Applications"
                            abstract="A high-definition (HD) digital twin framework, which provides a real-time and realistic visualization of multi-modal perception required for state estimation, navigation, and decision-making for autonomous driving, will be discussed and presented in this talk. We will introduce a perception system utilizing synchronized sensing data, the process to generate frame transformations to construct accurate HD maps for navigation in dynamic environments, and a framework to readily customize essential map elements such as road features and static landmarks. Application of the visualizer for localization tasks will also be demonstrated."/>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="15:00 - 15:30">
                        <Speaker
                            name="Matthew E. Taylor" affiliation="University of Alberta"
                            title="Integrating Reinforcement learning, with planning, control, and human input"
                            abstract="Reinforcement learning (RL) is a popular method for solving complex decision-making tasks, particularly when the full problem is unknown at design time. However, RL agents learning from scratch may require much more data than is readily available. In this talk, we will discuss how planning, control methods, and human intervention can be leveraged to quickly learn high-quality control polices that can outperform other methods, and how such methods could be applied to problems in autonomous driving."/>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="15:30 - 16:00" vertical={false}>
                        <p>Coffee Break</p>
                    </ProgramTableEntry>

                    <ProgramTableEntry time="16:00 - 16:30">
                        <Speaker
                            name="Randy Goebel and Shahin Atakishiyev" affiliation="University of Alberta"
                            title="Robustness Analysis of Interactive Explanations for Traffic Scene Understanding: Implications for Trust in Autonomous Driving"
                            />
                    </ProgramTableEntry>

                    <ProgramTableEntry time="16:30 - 17:00">
                        <Speaker
                            name="Harish Chintakunta" affiliation="MathWorks"
                            title="Developing Scenes and Scenarios in Automated Driving Applications"
                            abstract="The development of scenes and scenarios plays a crucial role in the design and testing of automated driving applications. This presentation will explore the workflows used to create interoperable scenes and scenarios with commonly used driving simulation tools. We will cover designing scenes, building scenarios from recorded data, and simulating driving applications for early design and testing phases."
                            />
                    </ProgramTableEntry>

                    <ProgramTableEntry time="17:00 - 17:30" vertical={false}>
                        <p><b>Panel Discussion</b></p>
                        <p>Moderated by Ehsan Hashemi</p>
                    </ProgramTableEntry>
                </ProgramTable>
            </div>
        </Section>
        
        <Section title="Organizers">           
            <div class="flex flex-col md:flex-row items-start md:items-center justify-evenly space-y-4 md:space-y-0 md:space-x-8 px-4 mx-auto">
                <Contact
                    name="Mohammad H. Mamduhi"
                    affiliation="University of Alberta"
                    email="vahid.mamduhi@gmail.com"
                    image="https://ieee-itsc.org/2024/wp-content/uploads/sites/3/2024/03/Mamduhi-150x150.png"/>
                <Contact
                    name="Ehsan Hashemi"
                    affiliation="University of Alberta"
                    email="ehashemi@ualberta.ca"
                    image="https://ieee-itsc.org/2024/wp-content/uploads/sites/3/2024/03/hashemi-768x768.png"/>
            </div>
        </Section>

    </Theme>
</div>
  