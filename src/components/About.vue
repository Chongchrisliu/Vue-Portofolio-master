<template>
    <section id="about" class="bg-color py-5 text-light">
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <img 
                        style="width:250px;height:auto;" 
                        src="https://images.pexels.com/photos/927451/pexels-photo-927451.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260"/>
                    <div v-for="(item, index) in items" :key="index" class="d-flex mt-2">
                        <i class="fas fa-1x mt-1" :class="'fa-'+item.icon"></i>
                        <span class="text-uppercase ml-3">{{item.name}}</span>
                    </div>
                </div>
                <div class="col-8">
                    <h3>About Me</h3> 
                    <h5>I am a Front End developer with industry experience building websites and web applications.</h5> 
                    <h5>I am a Front End developer with industry experience building websites and web applications.</h5> 
                    <div class="row">
                        <div class="col-6">
                            <h4>Contact Info.</h4> 
                            <h5>Chong Chris Liu</h5>
                            <h5>39 Gloxinia Cres, Toronto, M1W 2C3</h5>
                            <h5>1-647-993-0511</h5>
                            <h5>chongchrisliu@gmail.com</h5>
                        </div>
                        <div class="col-6">
                            <h3>download resume</h3> 
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
            items: [{icon: 'wrench', name: 'Hard Working', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'},
            {icon: 'graduation-cap', name: 'active-Learning', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'},
            {icon: 'handshake', name: 'Reliable', description:'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit molestias odio vero maxime fuga, doloremque magnam vel enim iusto alias?'}] 
        }
    }
}
</script>
<style scoped>
    .bg-color{
        background-color:rgba(209, 128, 3, 0.9);
    }
</style>
