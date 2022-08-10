<template>
    <v-app id="inspire">
        <v-app-bar app elevation="0">
            <v-subheader><h1 class="green--text">Shohan<span class="pink--text">@Portfolio</span></h1></v-subheader>
            <v-tabs center-active right background-color="transparent" active-class="active-tab">
                <v-tab href="#home">Home</v-tab>
                <v-tab>About</v-tab>
                <v-tab>Portfolio</v-tab>
                <v-tab>Experience</v-tab>
                <v-tab>Contact</v-tab>
            </v-tabs>
            <v-btn large color="green" class="white--text ml-10">Send me an Email</v-btn>
        </v-app-bar>
        <v-main style="background-color: #F5F5F5">
            <section class="intro-section" id="home">
                <v-row class="align-center px-10" style="height: 690px">
                    <v-col lg="6" cols="6" class="pa-6 font-weight-bold py-16">
                        <h2 class="display-3">Graphics <span class="green--text">Designer</span> & <span class="pink--text">Web</span>
                            Developer</h2>
                        <v-subheader>Hi, I am Shohanuzzaman, focusing on creative design.</v-subheader>
                        <br>
                        <br>
                        <v-btn large elevation="5" color="green" class="white--text mt-10 px-10 py-5">Hire Me</v-btn>
                        <v-btn large elevation="5" color="pink" class="white--text mt-10 ml-10 px-10 py-5">Contact
                        </v-btn>
                        <v-row class="mt-16">
                            <v-chip class="px-4 ma-3" color="#16A6FB">
                                <v-icon left size="20">mdi-facebook</v-icon>
                                Facebook
                            </v-chip>
                            <v-chip class="px-4 ma-3 white--text" color="#0A66C2">
                                <v-icon left size="20">mdi-linkedin</v-icon>
                                Linkedin
                            </v-chip>
                            <v-chip class="px-4 ma-3" color="#9DF3D3">
                                <v-icon left size="20">mdi-github</v-icon>
                                GitHub
                            </v-chip>
                        </v-row>
                    </v-col>
                    <v-col lg="6" cols="6">
                        <v-img src="https://i.postimg.cc/Gpf10PRc/shohan.png"></v-img>
                    </v-col>
                </v-row>
            </section>
            <section class="about-me" id="about">
                <v-img class="pa-10" height="400" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
                    <v-row justify="center" class="align-center">
                        <v-col lg="6" cols="6">
                            <v-card class="text-center pa-4 rounded-lg" color="#e1e0e0c9" elevation="6">
                                <v-chip class="ma-2" color="success" outlined>
                                    <v-icon left>
                                        mdi-account-circle
                                    </v-icon>
                                    ABOUT MYSELF
                                </v-chip>
                                <h2 class="display-1 font-weight-regular">
                                    Strong in design and integration with intuitive problem-solving skills. Skilled with HTML, CSS, Javascript, Vuejs, Vuetify, PHP & Adobe Creative
                                    Suite..
                                </h2>
                                <v-btn large elevation="5" color="pink" class="white--text mt-10 px-10 py-5">Download
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
                        
                            <v-card class="pa-6 rounded-xl mx-auto" max-width="700" elevation="5">
                                <div class="d-flex align-center justify-space-between">
                                    <div class="">
                                        <h2>Information & Communication Engineering</h2>
                                        <span>April 2015 - August 2020</span>
                                    </div>
                                    <a class="green--text">at Noakhali Science & Technology University <v-icon color="green">mdi-link</v-icon></a>
                                </div>
                                <v-card-text>
                                    <h3>Project</h3>
                                        Remote Desktop Application:
                                        This is a desktop application in which user can share their computer interface and control the computer remotely
                                        through the internet. I used C# and microsoft RDP client protocol. Through the RDP protocol an user can transfer large
                                        file over the internet. It solves many problems when someone want to control his home computer from office computer.
                                        Tools: C#, ASP.NET, SQL server, Microsoft RDP
                                        Github: RDP-Pro
                                </v-card-text>
                            </v-card>
                        
                    </v-row>
                </v-container>
            </section>
            <section class="experiance py-6">
                <v-img class="pa-10" height="550" gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                       src="https://designshack.net/wp-content/uploads/Home-office.jpg">
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
                                        <b>{{exper.date}}</b><br>
                                        <b>@{{exper.institute}}</b><br>
                                        {{exper.decription}}
                                    </v-card-text>
                                </v-card>
                            </v-timeline-item>
                        </v-timeline>
                    </v-container>
                </v-img>

            </section>
            <section class="portfolio">
                <h4 class="display-2 text-center">Portfolio</h4>
                <v-container>
                    <v-row justify="center">
                        <v-col lg="12">
                            <div class="text-center">
                                <v-chip @click="activeprotfolio = 'webapp'" :color="activeprotfolio == 'webapp'? 'success': ''" class="mx-5">Web App</v-chip>
                                <v-chip @click="activeprotfolio = 'desktopapp'" :color="activeprotfolio == 'desktopapp'? 'success': ''" class="mx-5">Desktop App</v-chip>
                                <v-chip @click="activeprotfolio = 'graphicsdesign'" :color="activeprotfolio == 'graphicsdesign'? 'success': ''" class="mx-5">Graphics Design</v-chip>

                            </div>
                        </v-col>
                        <slot v-if="activeprotfolio == 'desktopapp'">
                            <v-col lg="6">
                                <v-card
                                    :loading="loading"
                                    class="mx-auto my-12"
                                    max-width="500">

                                <v-img
                                height="250"
                                src="https://i.postimg.cc/KYyvj6pK/RDP-projects1.png"
                                ></v-img>

                                <v-card-title>RDP Desktop APP</v-card-title>

                                <v-card-text>
                                <v-row
                                    align="center"
                                    class="mx-0"
                                >
                                </v-row>
                                <br>
                                <div>This is a desktop application in which user can share their computer interface and control the computer remotely
                                    through the internet. I used C# and microsoft RDP client protocol. Through the RDP protocol an user can transfer large
                                    file over the internet. It solves many problems when someone want to control his home computer from office computer.</div>
                                </v-card-text>

                                <v-divider class="mx-4"></v-divider>

                                <v-card-title>Technology Used</v-card-title>

                                <v-card-text>
                                <v-chip-group
                                    v-model="selection"
                                    active-class="deep-purple accent-4 white--text"
                                    column
                                >
                                    <v-chip>C#</v-chip>

                                    <v-chip>ASP.NET</v-chip>

                                    <v-chip>SQL server</v-chip>

                                    <v-chip>Microsoft RDP</v-chip>
                                </v-chip-group>
                                </v-card-text>

                                <v-card-actions>
                                    <v-btn
                                        color="deep-purple lighten-2"
                                        text
                                        @click="reserve"
                                    >
                                        <a href="https://github.com/shohanuzzaman/RDP-Pro">GitHub</a> 
                                    </v-btn>
                                </v-card-actions>
                            </v-card>
                            </v-col>
                        </slot>

                        <slot v-if="activeprotfolio == 'webapp'">
                            <v-col lg="6">
                                <v-card
                                    :loading="loading"
                                    class="mx-auto my-12"
                                    max-width="500">

                                <v-img
                                height="250"
                                src="https://i.postimg.cc/KzMQZsj8/dokanpat-project.png"
                                ></v-img>

                                <v-card-title>E-Commerece Web APP</v-card-title>

                                <v-card-text>
                                <v-row
                                    align="center"
                                    class="mx-0"
                                >
                                </v-row>
                                <br>
                                <div>This is an e-commerce website in which user can buy various product and pay online.</div>
                                </v-card-text>

                                <v-divider class="mx-4"></v-divider>

                                <v-card-title>Technology Used</v-card-title>

                                <v-card-text>
                                <v-chip-group
                                    v-model="selection"
                                    active-class="deep-purple accent-4 white--text"
                                    column
                                >
                                    <v-chip>WordPress</v-chip>

                                    <v-chip>Html5</v-chip>

                                    <v-chip>Css3</v-chip>

                                    <v-chip>Javascript</v-chip>

                                    <v-chip>PHP</v-chip>
                                </v-chip-group>
                                </v-card-text>

                                <v-card-actions>
                                    <v-btn
                                        color="deep-purple lighten-2"
                                        text
                                        @click="reserve"
                                    >
                                        <a href="https://dokanpat.com.bd/">Visit Website</a>
                                    </v-btn>
                                </v-card-actions>
                            </v-card>
                            </v-col>
                        </slot>
                        
                    </v-row>
                </v-container>
                
                <slot v-if="activeprotfolio == 'graphicsdesign'">
                <v-slide-group
                        class="pa-4"
                        active-class="success"
                        show-arrows
                >
                    <v-slide-item v-for="(slider,index) in sliders" :key="index">
                        <v-card height="250" width="250" class="mx-2">
                            <img height="100%" width="100%" :src="slider" alt="">
                        </v-card>
                    </v-slide-item>
                </v-slide-group>
                </slot>
            </section>
            <section class="contact-us pt-10">
                <v-img class="pt-10" gradient="to bottom, rgb(166 199 156), rgb(227 227 227 / 86%)" src="https://img.freepik.com/free-photo/contact-us_36325-2135.jpg?size=626&ext=jpg">
                    <v-container>
                        <h4 class="display-1 text-center mb-5">
                            I’m a designer, based in Dhaka. Currently a freelancer. You can see my hobbies on behance @mdshoharnob and some photos on me too.
                        </h4>
                        <v-divider />
                        <br>
                        <v-row>
                            <v-col cols="12" lg="6">
                                <v-card-title>DROP A LINE</v-card-title>
                                <v-form>
                                    <v-text-field label="Your Name" />
                                    <v-text-field label="Email" />
                                    <v-text-field label="Subject" />
                                    <v-textarea label="Message" />
                                    <v-btn large color="green" class="white--text">Send Message</v-btn>
                                </v-form>
                            </v-col>
                            <v-col cols="12" lg="3" offset="2">
                                <v-card-title>CONTACT ME</v-card-title>
                                <v-card-text>
                                    Block-B, Mirpur-06, Dhaka <br>
                                    +8801788408835 <br>
                                    arnob77s@gmail.com <br>
                                </v-card-text>
                                <v-card-actions>
                                    <v-btn large elevation="5" color="pink" class="white--text mt-10 px-10 py-5">Download
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
                                <a href="" class="green--text">SHOHANUZZAMAN</a>
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
            activeprotfolio: 'webapp',
            drawer: null,
            items: [
                {title: 'HTML', value: 100, color: 'light-blue'},
                {title: 'CSS', value: 100, color: 'deep-orange'},
                {title: 'Javascript', value: 70, color: 'light-green'},
                {title: 'Vuejs', value: 80, color: 'blue'},
                {title: 'Vuetify', value: 90, color: 'black'},
                {title: 'PHP', value: 50, color: 'red'},
            ],
            experience: [
                {
                    title: 'Web Developer',
                    date: 'November 2020 - April 2021',
                    institute: 'Sristy Samajik Unayan Sanastha',
                    decription: 'Worked with WordPress, Html5, Css3, Javascript, PHP. Made a e-commerce website named dokanpat.com'
                },
                {
                    title: 'Graphics Designer',
                    date: 'Agust 2020 - May 2022',
                    institute: 'Expo Group BD',
                    decription: 'Worked as a graphics designer and RPA developer'
                },
            ],
            alignments: [
                    'center'
                    
            ],
            sliders:[
                'https://i.postimg.cc/MZdqsQDW/Psychopathy-course.png',
                'https://i.postimg.cc/ryt74RPn/promoads-poster.png',
                'https://i.postimg.cc/MGppZmtr/i-miss-Lionel-Messi-removebg-preview.png',
                'https://i.postimg.cc/PfWsc8QL/Gym.jpg',
                'https://cdn.dribbble.com/users/702789/screenshots/14012516/media/561a8b7e8cbe51c72c18f4ef0dc72676.png?compress=1&resize=400x300',
                'https://cdn.dribbble.com/users/2399102/screenshots/15522177/media/346d890482d929610d316938e7d48629.png?compress=1&resize=400x300',
            ]
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
</style>