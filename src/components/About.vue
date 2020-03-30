<template>
    <section id="about" class="bg-color padding-bg text-light">
        <div class="container">
            <div class="row">
                <div class="col-md-4 col-12">
                    <img 
                        style="width:250px;height:auto;" 
                        src="https://images.pexels.com/photos/927451/pexels-photo-927451.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"/>
                </div>
                <div class="col-md-8 col-12">
                    <h3 class="mb-3">About Me</h3> 
                    <div>I am a Front End developer with industry experience building websites and web applications.</div> 
                    <div class="mt-2">I am a Front End developer with industry experience building websites and web applications.</div>
                    <div class="row mt-4">
                        <div class="col-6">
                            <h3 class="mb-3">Contact Details</h3> 
                            <div>
                                <div>Chong Chris Liu</div>
                                <div class="mt-2">39 Gloxinia Cres, Toronto, M1W 2C3</div>
                                <div class="mt-2">1-647-993-0511</div>
                                <div class="mt-2">chongchrisliu@gmail.com</div>
                            </div>

                        </div>
                        <div class="col-6">
                            <div> <span class="h3">Download Resume</span><i class="fas fa-download fa-lg ml-2"></i></div> 
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
            items: [
                {icon: 'wrench', name: 'Hard Working', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'},
                {icon: 'graduation-cap', name: 'active-Learning', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'},
                {icon: 'handshake', name: 'Reliable', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'}
            ] 
        }
    }
}
</script>
<style scoped>
    .bg-color{
        background-color:rgba(209, 128, 3, 0.9);
    }
    .padding-bg{
        padding-top: 80px;
        padding-bottom: 80px;
    }
</style>
