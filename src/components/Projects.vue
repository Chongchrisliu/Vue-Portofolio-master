<template>
    <section id="projects" class="padding-bg">
        <div class="container">
            <div class="text-center h5"><span >CHECK OUT SOME OF MY WORKS</span> <i class="fas fa-tasks"></i> </div> 
            <div class="row mt-4">
                <div v-for="(item, index) in items" :key="index" class="mt-5">
                    <div class="row">
                        <div  class="mb-3 col-md-4 col-12"><img  :src="item.image1" :alt="item.name" class="img-fluid rounded" ></div>
                        <div  class="mb-3 col-md-4 col-12"><img  :src="item.image2" :alt="item.name" class="img-fluid rounded" ></div>
                        <div  class="mb-3 col-md-4 col-12"><img  :src="item.image3" :alt="item.name" class="img-fluid rounded" ></div>
                    </div>
                    <div class="mt-3">
                        <div class="h3">{{item.name}}</div>
                        <div class="text-secondary mt-3" style="font: italic 1em Georgia, serif;">
                            {{item.company}}      
                            {{item.job}}  
                        </div>  
                        <div class="mt-3" type="button" data-toggle="collapse" :data-target="item.target" aria-expanded="false"> 
                            <span>
                                {{item.skills}}
                            </span>    
                            <i class="fas fa-chevron-circle-down text-primary float-right" style="font-size:20px;" ></i>     
                        </div>
                    </div>
                        
                    <div class="collapse" :id="item.targetid" >
                        <div class="card-body card card-bg">
                            {{item.jobdescription}}
                        </div>     
                    </div>
                    <div class="mt-4">
                        <hr>
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
                    image1: image1, 
                    image2: image2, 
                    image3: image3, 
                    name: 'Dating Website', 
                    job: "Front-end Developer.",
                    company: "Somoplay.",
                    skills: "Vue, JavaScript, HTML/CSS, Sass, Element-UI, Bootstrap.",
                    target: "#projectone",
                    targetid: "projectone",
                    jobdescription: "haaaaaaaaaaaaa"
                },
                {
                    image1: image1, 
                    image2: image2, 
                    image3: image3, 
                    name: 'Dating Website', 
                    job: "Front-end Developer.",
                    company: "Somoplay.",
                    skills: "Vue, JavaScript, HTML/CSS, Element-UI.",
                    target: "#projecttwo",
                    targetid: "projecttwo",
                    jobdescription: "haaaaaaaaaaaaa"
                },
                {
                    image1: image1, 
                    image2: image2, 
                    image3: image3, 
                    name: 'Dating Website', 
                    job: "Front-end Developer.",
                    company: "Somoplay.",
                    skills: "Vue, JavaScript, HTML/CSS, Element-UI.",
                    target: "#projectthree",
                    targetid: "projectthree",
                    jobdescription: "haaaaaaaaaaaaa"
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
        letter-spacing: 0.03em;
    }
    .card-bg{
        background-color:transparent;
    }
</style>
