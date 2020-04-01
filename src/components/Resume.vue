<template>
    <section id="resume" class="padding-bg bg-light">
        <div class="container" style="text-align:justify; text-justify:inter-ideograph;">
            <div class="row">
                <div class="col-12 col-md-4 mb-4" >
                    <span class="border-3 border-warning h3">Education</span> 
                </div>
                <div class="col-12 col-md-8 mt-2" >
                    <div v-for="(education, index) in educations" :key="index">
                        <hr v-if="index !==0" style="margin-top:30px;margin-bottom:30px;">
                        <div class="row">
                            <div class="h4 col-9">
                                <span >{{education.school_title}}</span> 
                            </div>
                            <div class="col-3">
                                <span class="float-right" style="font: 1.1em Georgia, serif;">{{education.school_country}}</span>
                            </div>    
                        </div>
                        <p class="h5 mt-3" style="font: italic 1em Georgia, serif;">{{education.department_title}}</p> 
                        <p v-if="education.degree_title !== ''" class="h6 mt-2" style="font: italic 1em Georgia, serif;">{{education.degree_title}}, {{education.gradaute_date}}.</p> 
                        <p class="h6 mt-4">{{education.experience}}</p>
                    </div>
                </div>
            </div>
            <hr class="hr">
            <div class="row mt-5">
                <div class="col-md-4 col-12 h3 mb-4" >
                    <span class="border-3 border-warning">Work</span> 
                </div>
                <div class="col-md-8 col-12 mt-2" >
                    <div v-for="(work, index) in works" :key="index">
                        <hr v-if="index !== 0" style="margin-top:30px;margin-bottom:30px;">
                        <p class="h4">{{work.place_title}}</p> 
                        <p class="h5 mt-3" style="font: italic 1em Georgia, serif;">{{work.position_title}}</p> 
                        <p class="h6 mt-4">{{work.job_description}}</p>    
                    </div>
                </div>
            </div>
            <hr class="hr">
            <div class="row mt-5">
                <div class="col-md-4 col-12 h3 mb-4" >
                    <span class="border-3 border-warning">Skills</span> 
                </div>
                <div class="col-md-8 col-12" >
                    <p class="h6">
                        {{skills.description}}
                    </p> 
                    <div v-for="(item, index) in skills.items" :key="index" class="mt-4">
                        <span style="font-weight:700;">
                            {{item.title}}
                        </span>
                        <div class="progress mt-2" style="height: 25px;">
                            <div :class="item.color" class="progress-bar progress-bar-striped" role="progressbar" style="width: 100%;" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
                        </div>
                    </div>                
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data () {
        return {
            skills:{
                description: "The main skill sets below outline the variety of skills performed within roles as a developer during past experience in University of Waterloo and Somoplay Inc..",
                items: [
                    {
                        title: "Javscript / ES6",
                        color:"bg-primary",
                    },
                    {
                        title: "HTML5 / CSS3 / SASS",
                        color:"bg-success",
                    },
                    {
                        title: "Vue / React",
                        color:"bg-primary",
                    },
                    {
                        title: "Java / Spring",
                        color:"bg-success",
                    },
                    {
                        title: "SQL / MySQL / Amazon S3",
                        color:"bg-primary",
                    },
                    {
                        title: "RESTful API",
                        color:"bg-success",
                    },
                    {
                        title: "MVC / Responsive Web Design",
                        color:"bg-primary ",
                    },
                ]
            },

            works:[
                {
                    place_title: "Somoplay Inc.",
                    position_title: "Front-End Developer",
                    job_description: "working experience",
                },
                {
                    place_title: "University of Waterloo",
                    position_title: "Research Assistant",
                    job_description: "working experience",
                }
            ],

            educations:[
                {
                    school_title: "University of Waterloo",
                    school_country: "Canada",
                    department_title: "Electrical and Computer Engineering",
                    degree_title: "Master of Appleid Science",
                    gradaute_date: "June, 2019",
                    experience:"study experience",
                },
                {
                    school_title: "North China Electric Power University",
                    school_country: "China",
                    department_title: "Computer Science",
                    degree_title: "",
                    gradaute_date: "",
                    experience:"study experience",
                }
            ]
        }
    }
}
</script>

<style>
    .hr { 
        display: block;
        height: 1px;
        border: 0; 
        border-top: 1px solid #ccc;
        margin-top: 40px;
        margin-bottom: 40px;
    }
    .padding-bg{
        padding-top: 80px;
        padding-bottom: 80px;
        letter-spacing: 0.03em;
    }
    .border-3{
        border-bottom: 3px solid;
    }
</style>