<template>
    <section id="social">
        <div class="container padding-bg">
            <div class="text-center">
                <i class="fas fa-envelope fa-lg"></i>
                <span class="h5 ml-2">{{title1}}</span>  
                <p class="text-primary mt-2" style="font-size:14px;">{{title2}}</p>  
            </div> 
            <div class="row" style="margin-top:60px;">
                <div class="col-md-4 col-12 mb-4">
                    <img class="image-size" :src="logo"/>
                </div>
                <div class="col-md-8 col-12">
                    <el-form :model="ruleForm" :rules="rules" label-position="left" ref="ruleForm" label-width="25%" class="demo-ruleForm">
                        <el-form-item label="Name" prop="name">
                            <el-input placeholder="Please input your name"  v-model="ruleForm.name">
                                <i class="far fa-edit mr-1" slot="suffix"></i>
                            </el-input>
                        </el-form-item>
                        <el-form-item label="E-mail" prop="email" class="mt-3">
                            <el-input placeholder="Please input your email" v-model="ruleForm.email">
                                <i class="fas fa-envelope mr-1" slot="suffix"></i>
                            </el-input>
                        </el-form-item>
                        <el-form-item label="Message" prop="message" class="mt-3">
                            <el-input placeholder="Please input the message" type="textarea" v-model="ruleForm.message" :autosize="{ minRows: 4, maxRows: 10}"></el-input>
                        </el-form-item>
                        <el-form-item class="mt-4">
                            <el-button type="warning" @click="submitForm('ruleForm')">Send<i class="far fa-paper-plane ml-1"></i></el-button>
                        </el-form-item>
                    </el-form>
                </div>
                
            </div>       
        </div>
    </section>
</template>

<script>
import authorlogo from '../assets/img/author_logo.jpeg'
  export default {
    data() {
      return {
        title1:"Please feel free to contact me and I will return your email so we can keep in touch.",
        title2: "Please fill out the form and note * items are required before submission.",
        ruleForm: {
          name: '',
          email:'',
          message: ''
        },
        rules: {
          name: [
            { required: true, message: 'Please input your name', trigger: 'blur' },
            { min: 1, max: 20, message: 'Length should be 1 to 20', trigger: 'blur' }
          ],
          email: [
            { required: true, message: 'Please input your email', trigger: 'blur' },
          ],
          message: [
            { required: true, message: 'Please input message', trigger: 'blur' }
          ]
        },
        logo: authorlogo
      };
    },
    methods: {
      submitForm(formName) {
        this.$refs[formName].validate((valid) => {
          if (valid) {
            alert('submit!');
          } else {
            console.log('error submit!!');
            return false;
          }
        });
      },
      resetForm(formName) {
        this.$refs[formName].resetFields();
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
     .image-size {
        width:auto;
        height:auto;
        max-width:100%;
        max-height:100%;
    }
</style>
