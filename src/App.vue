<template>
    <v-app id="inspire">
        <v-app-bar app elevation="0">
            <v-subheader><h1 class="black--text">My<span class="orange--text">Portfolio</span></h1></v-subheader>
            <v-tabs center-active right background-color="transparent" active-class="active-tab">
                <v-tab><a href="#home" style="text-decoration: none"></a>Home</v-tab>
                <v-tab><a href="#about" style="text-decoration: none">About</a></v-tab>
                <v-tab><a href="#project" style="text-decoration: none">Project</a></v-tab>
                <v-tab><a href="#contact" style="text-decoration: none">Contact</a></v-tab>
            </v-tabs>
        </v-app-bar>
        <v-main style="background-color: #F5F5F5">
            <section class="intro-section" >
                <v-row class="align-center px-10" style="height: 690px">
                    <v-col lg="6" cols="6" class="pa-6 font-weight-bold py-16" id="home">
                        <h2 class="display-3">Front <span class="green--text">End</span> <span class="pink--text">Web</span>
                            Developer</h2>
                        <v-subheader>Hi, I am Syed Nazmul Hossain, focusing on creating emotional experiences.</v-subheader>
                        <br>
                        <br>
                        <v-btn large elevation="5" color="green" class="white--text mt-10 px-10 py-5">Hire Me</v-btn>
                        <v-btn large elevation="5" color="pink" class="white--text mt-10 ml-10 px-10 py-5" href="#contact">Contact
                        </v-btn>
                        <v-row class="mt-16">
                           
                            <v-chip class="px-4 ma-3" color="info" href="https://www.linkedin.com/in/syed-nazmul-hossain/" target="_blank">
                                <v-icon left size="20">mdi-linkedin</v-icon>
                                Linkedin
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="dark" href="https://github.com/nazmulhossain17" target="_blank">
                                <v-icon left size="20">mdi-github</v-icon>
                                Github
                            </v-chip>
                        </v-row>
                    </v-col>
                    <v-col lg="6" cols="6">
                        <v-img src="https://i.ibb.co/Dt3DTY6/289404966-746389866778668-8556477145616495666-n.jpg" width="600px"></v-img>
                        <br>
                    </v-col>
                </v-row>
                <br>
                <br>
            </section>
            <section class="about-me" id="about">
                <v-img class="pa-10" height="400" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-row justify="center" class="align-center">
                        <v-col lg="6" cols="6">
                            <v-card class="text-center pa-6 rounded-lg" color="#e1e0e0c9" elevation="6" id="about">
                                <v-card-subtitle class="green--text">ABOUT MYSELF</v-card-subtitle>
                                <h2 class="display-1 font-weight-regular">
                                    Hard-working individual with proficiency in HTML, CSS, JavaScript, and, MERN as well as ability to communicate effectively in a team setting, and possessing a strong willingness. 
                                    
                                </h2>
                                <v-btn large elevation="5" color="blue" class="white--text mt-10 px-10 py-5" href="https://drive.google.com/file/d/1pEZCsQkfP-ix7qyc-VwKjAF6j_6-9c5x/view" target="_blank">Download
                                    Resume
                                    <v-icon>mdi-download</v-icon>
                                </v-btn>
                            </v-card>
                        </v-col>
                        <v-col lg="6" cols="6">
                            <v-card class="pa-6 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <div class="py-1" v-for="(item,index) in items" :key="index">
                                    <label>{{ item.title }}</label>
                                    <v-progress-linear
                                            :color="item.color"
                                            height="10"
                                            :value="item.value"
                                    ></v-progress-linear>
                                </div>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-img>
            </section>
            <section class="educaion py-6">
                <v-container>
                    <h4 class="display-2 text-center">Education</h4>
                    <v-row class="py-8">
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>HSC Passed</h2>
                                        <span>Passing Year - 2021</span>
                                    </div>
                                    <a class="green--text">at JU School & College </a>
                                </div>
                                <v-card-text>
                                    I have passed HSC exam in Science Group from Jahangernogor Universite School & College in 2021.
                                </v-card-text>
                            </v-card>
                        </v-col>
                        <v-col cols="12" lg="6">
                            <v-card class="pa-6 rounded-xl " elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>SSC Passed</h2>
                                        <span>Passing Year - 2019</span>
                                    </div>
                                    <a class="green--text">at M.A. Latif School</a>
                                </div>
                                <v-card-text>
                                    I have passed HSC exam in Science Group from M.A Latif Memorial School in 2019.
                                </v-card-text>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-container>
            </section>
            <section class="experiance py-6">
                <v-img class="pa-10" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://images.unsplash.com/photo-1461782296610-c552d61b149a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1576&q=80">
                    <v-container>
                        <h4 class="display-2 text-center">Experience</h4>
                        <v-timeline>
                            <v-timeline-item v-for="(exper,index) in experience" :key="index"
                                             :color="index % 2 === 0 ?'pink':'green'">
                                <v-card class="rounded-xl">
                                    <v-card-title :color="index % 2 === 0 ?'pink':'green'">
                                        {{exper.title}}
                                    </v-card-title>
                                    <v-card-text>
                                        {{exper.decription}}
                                    </v-card-text>
                                </v-card>
                            </v-timeline-item>
                        </v-timeline>
                    </v-container>
                </v-img>

            </section>
            <section class="portfolio">
                <h4 class="display-2 text-center">PROJECTS</h4>
                <br>
              <v-col cols="12" id="project">
                <div class="child bgColor1">
                  
                  <h3 class="white--text ml-3 mt-4">Password-Generator</h3>
                  <p class="grey--text ml-3 mt-6">
                    Passwords are a real security threat.<br />
                    So if you want to safeguard your personal info and assets, <br>
                    creating secure passwords is a big first step. <br>
                    And that's where my Password Generator can help.
                  </p>
                  <v-btn color="#317f0f" dark text href="https://nazmulhossain91-passwordgen.netlify.app/" target="_blank">
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
                <div class="child bgColor2">
                  <h3 class="white--text ml-3 mt-4">PingPong Game</h3>
                  <p class="black--text ml-3 mt-6">
                    The game involves two paddles and a moving ball.
                    The players <br>have to move paddles in an upwards or
                    downwards direction <br> and save the ball from getting hit onto the wall.
                    If the ball <br>hits the wall then it's a score for another player.
                  </p>
                  <v-btn color="pink" dark text href="https://nazmul-pingpong-game.netlify.app/" target="_blank">
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
                <div class="child bgColor1">
                  <h3 class="white--text ml-3 mt-4">Unlimited Quote Gen</h3>
                  <p class="grey--text ml-3 mt-6">
                    I build a Quote generator using JavaScript. 
                    This Quote Generator <br>application has button when clicked
                    it shows new quotes. On click <br> of the New Quote button, 
                    the next quote will be generated <br>through request.
                  </p>
                  <v-btn color="#ecb81b" dark text href="https://unlimited-quote.netlify.app/" target="_blank">
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
                
              </v-col>
            </section>
            <section class="contact-us pt-10">
                <v-img class="pt-10" gradient="to bottom, rgb(255,0,255), rgb(227 227 227 / 86%)" src="https://img.freepik.com/free-photo/contact-us_36325-2135.jpg?size=626&ext=jpg">
                    <v-container>
                        <h4 class="display-1 text-center mb-5">
                            I’m a Web Developer, based in Dhaka Bangladesh. Currently i'm a student. I'm a self-taught, energetic learner and developer.
                        </h4>
                        <v-divider />
                        <br>
                        <v-row>
                            <v-col cols="12" lg="6">
                                <v-form>
                                    <v-text-field label="Your Name" />
                                    <v-text-field label="Email" />
                                    <v-text-field label="Subject" />
                                    <v-textarea label="Message" />
                                    <v-btn large color="green" class="white--text">Send Message</v-btn>
                                </v-form>
                            </v-col>
                            <v-col cols="12" lg="3" offset="2" id="contact">
                                <v-card-title>CONTACT ME</v-card-title>
                                <v-card-text>
                                    Dosaid Bazar,Savar Dhaka, Bangladesh <br>
                                    +880 1991202867 <br>
                                    nazmulhossain17sn@gmail.com <br>
                                </v-card-text>
                                <v-card-actions>
                                    <v-btn large elevation="5" color="blue" class="white--text mt-10 px-10 py-5" href="https://drive.google.com/file/d/1pEZCsQkfP-ix7qyc-VwKjAF6j_6-9c5x/view" target="_blank">Download
                                        Resume
                                        <v-icon>mdi-download</v-icon>
                                    </v-btn>
                                </v-card-actions>
                            </v-col>
                        </v-row>
                    </v-container>
                    <v-footer class="mt-4">
                        <v-col
                                class="text-center"
                                cols="12"
                        >
                            <strong>Copyright ©{{ new Date().getFullYear() }} All rights reserved | This is made by
                                <a href="" class="green--text">Syed Nazmul Hossain</a>
                            </strong>
                        </v-col>
                    </v-footer>
                </v-img>
            </section>
        </v-main>
    </v-app>
</template>

<script>
    export default {
        name: 'App',

        data: () => ({
            drawer: null,
            items: [
                {title: 'HTML', value: 100, color: 'light-blue'},
                {title: 'CSS', value: 100, color: 'deep-orange'},
                {title: 'Javascript', value: 70, color: 'light-green'},
                {title: 'ReactJs', value: 80, color: 'blue'},
                {title: 'MongoDB', value: 90, color: 'black'},
                {title: 'Linux', value: 100, color: 'red'},
            ],
            experience: [
                {
                    title: 'Web Development',
                    decription: "I have 4 years of experience of Web Development. And I'm still learning new technologies. I love to learn new technologies. And my goal is to be a professional web developer."
                },
                {
                    title: 'JavaScript',
                    decription: 'JavaScript is my favourite language. I love to build JavaScript projects. I love practicing JavaScript and making responsive website in JavaScript.'
                },
                {
                    title: 'React JS',
                    decription: "I have 1.5 years of experience of React Js. React is one of my favourite language. And I'm still learning advance react."
                },
                {
                    title: 'MongoDB',
                    decription: 'MongoDB is my favourite database backend language. I have 1 years of experience of that language.'
                },
            ],
            // sliders:[
            //     'https://i.ibb.co/Hr6pc6y/Screenshot-1.png',
            //     'https://cdn.searchenginejournal.com/wp-content/uploads/2019/12/5-ways-seo-web-design-go-together-5e2945dd5df37.png',
            //     'https://data.whicdn.com/images/350420216/original.jpg?t=1605047796',
            //     'https://1zylgb20pxi7mw2sdr8i4a14-wpengine.netdna-ssl.com/wp-content/uploads/2020/01/projectleft.jpg',
            //     'https://cdn.dribbble.com/users/702789/screenshots/14012516/media/561a8b7e8cbe51c72c18f4ef0dc72676.png?compress=1&resize=400x300',
            //     'https://cdn.dribbble.com/users/2399102/screenshots/15522177/media/346d890482d929610d316938e7d48629.png?compress=1&resize=400x300',
            // ]
        }),
    }
</script>
<style>
    .v-tab.active-tab {
        color: #e91e63;
    }

    .v-tab.active-tab::before {
        background-color: #4caf50;
    }
    .child {
        display: inline-block;
        padding: 2rem 1rem;
        vertical-align: middle;
        text-align: left;
        margin-right: 8px;
    }
    .bgColor1 {
        background-color: #1e1e1e;
    }
    .bgColor2 {
        background-color: #ce1d2a;
        }
        .child1 {
        display: inline-block;
        padding: 2rem 1rem;
        vertical-align: middle;
        margin-right: 5px;
        width: 240px;
        }
        .child2 {
        display: inline-block;
        width: 245px;
        vertical-align: middle;
        }
</style>