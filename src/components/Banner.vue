<template>
    <section id="banner">
        <div class="container">
            <div class="text-center height-100 align-middle">      
                <p class="text-white font-weight-bold" style="padding-top:35%;font-size:90px;">{{item.name}}</p>
                <p style="font-size:20px;color:white"> 
                    {{item.description}}
                </p>
                <p style="font-size:20px;color:gray">
                    {{item.subdescription_1}} <font class="text-primary">{{item.hightlight_skill_1}}</font> {{item.subdescription_2}}<font class="text-primary"> {{item.hightlight_skill_2}}</font> {{item.subdescription_3}} <font class="text-primary"> {{item.hightlight_skill_3}}</font>.
                </p>
                <hr>
                <div style="margin-top:47%;">
                    <button v-for="(icon, index) in icons" :key="index" type="button" class="btn btn-outline-primary btn-sm border-0 mr-2">
                        <i :class="icon.name" style="font-size:28px;"></i>
                    </button>
                </div>        
            </div>
        </div>
    </section>
</template>

<script>
export default {
   data () {
        return {
            item:{
                name: "Chong Chris Liu.",
                description: "I am a Front-End developer with industry experience building reactive websites and web applications.",
                subdescription_1: "I specialize in",
                subdescription_2: "and have professional experience working with",
                subdescription_3: "and",
                hightlight_skill_1: "JavaScript",
                hightlight_skill_2: "Vue",
                hightlight_skill_3: "React",
            },
            icons:[
                {name:"fab fa-facebook-f"},
                {name:"fab fa-github"},
                {name:"fab fa-linkedin-in"},
                {name:"fab fa-instagram"},
                {name:"fab fa-google"},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .scrolldown{
        color:white;
    }
</style>
