<template>
    <section id="projects" class="bg-light padding-bg">
        <div class="container">
            <div class="row">
                <div v-for="(item, index) in items" :key="index" class="mb-3 col-lg-4 col-6 col-xs-12">
                    <div><img :src="item.image" :alt="item.name" class="img-fluid rounded" ></div>
                    <hr>
                    <div class="mt-3">
                        <h3>{{item.name}}</h3>
                        <div class="text-secondary mt-3">
                            <span>
                                {{item.job}}
                            </span> 
                            <span class="float-right">
                                {{item.company}}
                            </span>       
                        </div>
                        <div class="mt-2"> 
                            <span class="font-italic">
                                {{item.skills}}
                                
                            </span>    
                            <span class="float-right">
                                <i class="fas fa-angle-down" type="button" data-toggle="collapse" :data-target="item.target" aria-expanded="false"></i>
                                
                            </span>     
                        </div>
                       
                        <div class="collapse" :id="item.targetid">
                            <div class="text-secondary">
                                {{item.jobdescription}}
                            </div>
                        </div>
                    </div>  
                </div>
            </div>
        </div>
    </section>
</template>
<script>
import image1 from '../assets/img/project1.jpg'
import image2 from '../assets/img/project2.jpg'
import image3 from '../assets/img/project3.jpg'

export default {
    data () {
        return {
            items: [
                {
                    image: image1, 
                    name: 'Dating Website', 
                    job: "Front-end Developer",
                    company: "Somoplay.",
                    skills: "Vue, JavaScript, HTML/CSS, Element-UI",
                    target: "#projectone",
                    targetid: "projectone",
                    jobdescription: "haaaaaaaaaaaaa"
                },
                {
                    image: image2, 
                    name: 'Project 2', 
                    job: "Full-Stack Developer",
                    company: "Somoplay.",
                    skills: "Vue",
                    target: "#projecttwo",
                    targetid: "projecttwo",
                    jobdescription: "haaaaaaaaaaaab"
                },
                {
                    image: image3, 
                    name: 'Project 3', 
                    job: "front-end",
                    company: "Somoplay.",
                    skills: "Vue",
                    target: "#projectthree",
                    targetid: "projectthree",
                    jobdescription: "haaaaaaaaaaaac"
                },
            ]
        }
    }
}
</script>

<style lang="scss">
    .padding-bg{
        padding-top: 80px;
        padding-bottom: 80px;
    }
</style>
