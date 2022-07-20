<template>

    <div class=" login_container col-lg-6 col-md-5">
        <div class="logo">
            <img src="../assets/img/logo.jpg" alt="">
        </div>
        <div class=" login_card d-flex aling-item-center justify-content-center">
            <div class="form_body ">
                <h1> Welcome back, Olivia</h1>
                <p>Welcome back! Please enter your details.</p>

                <div class="button_google btn"> 
                    <img class="img_google" src="../assets/img/google.svg" alt="google">
                    <span class="px-2 ">Log in with Google</span>
                </div>

                <div class="d-flex align-items-center my-3">
                    <hr class="hr_line"> 
                    <span class="px-2">or</span> 
                    <hr class="hr_line">
                </div>

                <form class="mt-5" action="#">
                    <div class="field_email">
                        <label for="form_email"></label>
                        <input class="w-100" placeholder="Email" type="email" id="form_email" required >
                    </div>
                    <div class="field_password my-3">
                        <label for="form_password" placeholder="Password"></label>
                        <input class="w-100" type="password" placeholder="Password" id="form_password" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" title="Must contain at least one number and one uppercase and lowercase letter, and at least 8 or more characters" required >
                    </div>
                    <div class="remember_help  w-100 text-start align-items-center d-flex justify-content-between">
                        <div class="align-items-center d-flex mx-2">
                            <input type="checkbox" id="remember_check" name="remember_check" value="Remember">
                            <label class="ps-2" for="remember_check"> Remember for 30 days</label>
                        </div>
                        <div>
                            <a class="forgot_password" href="#">Forgot password</a> 
                        </div>
                    </div>
                    <div class="button_login">
                        <button type="submit" class="btn mb-3">Log in</button>
                    </div>
                    <div class="sign-up_container">
                        <span>Don't have an account? </span> 
                        <a href="#"><strong>Sing up for free</strong> </a>
                        <img  src="../assets/img/decoration.png" alt="">
                    </div>
                </form>   
                
            </div>       
        </div>
    </div> 

</template>

<script>
export default {
    name:"Login ",
}
</script>

<style lang="scss" scoped>
    .login_container{
            overflow-y: auto;
            height: 100%;
            display: flex;
            flex-direction: column;
        a{
            color:black;
            font-weight: 600;
        }
        a:hover{
            cursor: pointer;
        }
        .login_card{
            align-items:center;
            width: 100%;
            height: 100%;
            .form_body{
                max-height: 100%;
                h1{
                    font-size: 1.5rem;
                    font-weight: 600;
                }
                p{
                    font-size: 12px; 
                    color:gray;
                }
                .button_google{
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    border: 1px solid lightgrey;
                    border-radius: .3125rem;
                    width:100%;
                    padding:.4rem;
                    .img_google{
                        width: 1.25rem;   
                    }
                }
                .sign-up_container{
                    position: relative;
                    text-align: center;
                    font-size: 0.7rem;
                    span{
                        color:grey 
                    }
                    a{
                        text-decoration: none;
                    }
                    img{
                        position: absolute;
                        top:1rem;
                        right:10px;
                        width: 7rem;
                    }
                }
            }
            .hr_line{
                width: 50%;
                background-color: lightgrey;
            }
            input{
                border: none;
                border-bottom: 1px solid lightgrey;
                padding: .5rem;
            }
            .remember_help{
                font-size: .65rem;
                padding: 0 .3125rem;
            }       
        }
        
        .logo{
            img{
                height: 4rem;
            }
        }
        
        
        .button_login{
            padding: 1.25rem 0;
            button{
                background-color:#111727 ;
                color: white;
                width:100%;
            }
        }
    }
</style>

