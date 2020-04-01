<template>
    <section id="about" class="bg-color padding-bg">
        <div class="container">
            <div class="row">
                <div class="col-md-4 col-12 mb-4">
                    <img 
                        class="image-size"
                        src="https://cdn.pixabay.com/photo/2015/10/07/22/54/pen-spinning-976930_1280.jpg"/>
                </div>
                <div class="col-md-8 col-12">
                    <span class="mb-3 h3">About Me</span> 
                    <div class="mt-4 description-font-fm" style="text-align:justify; text-justify:inter-ideograph;font-size:15px;">
                        <div>{{info.description_1}}</div> 
                        <div class="mt-2">{{info.description_2}}</div>
                        <div class="mt-2">{{info.description_3}}</div>
                    </div>
                    <div class="mt-4"> 
                        <hr>
                    </div>
                    <div class="row mt-4">
                        <div class="col-md-6 col-12 mb-4">
                            <span class="mb-3 h3">Contact Details</span> 
                            <div class="mt-3" style="text-align:justify; text-justify:inter-ideograph;font-size:15px;">
                                <div>{{info.contact_name}}</div>
                                <div class="mt-2">{{info.contact_address}}</div>
                                <div class="mt-2">{{info.contact_phone}}</div>
                                <div class="mt-2">{{info.contact_email}}</div>
                            </div>
                        </div>
                        <div class="col-md-6 col-12">
                            <button type="button" class="btn btn-dark float-md-right ">
                                <i class="fas fa-download ml-2 text-primary"></i>
                                <span class="ml-2" style="font-size:17px;"> Download Resume</span>
                            </button>
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
            info: {
                description_1: "Hands-on Technical Experience on Front-End(Client-side) Technologies Like HTML5, CSS3, JavaScript, SASS, MVC, And Responsive Web Design.",
                description_2: "Profound Knowledge in Vue/React Concepts Like Component-based Design, Routing, State Management: Vuex, Redux.",
                description_3: "Enriched Experience in Working with RESTful Web Services and implementing RESTful API's.",
                contact_name: "Chong Chris Liu",
                contact_address: "39 Gloxinia Cres, Toronto, Canada, M1W 2C3",
                contact_phone: "1-647-993-0511",
                contact_email: "chongchrisliu@gmail.com",
            },
        }
    }
}
</script>
<style scoped>
    .padding-bg{
        padding-top: 80px;
        padding-bottom: 80px;
        letter-spacing: 0.03em;
    }
    .image-size {
        width:200px;
        height:200px;
        max-width:80%;
        max-height:80%;
        overflow: hidden;
        border-radius: 50%;
    }
    @media screen and (max-width: 767px) {
        .image-size {
            max-width:100%;
            max-height:100%;
        }
    }
    
</style>
