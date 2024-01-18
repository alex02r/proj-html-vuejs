<script>
export default {
    
}
</script>
<template lang="">
    <footer class="pt-5">
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-3">
                    <div class="logo">
                        <img src="../assets/logo-footer-gobike.png" alt="Logo">
                    </div>
                    <ul class="list-footer">
                        <li><i class="fas fa-location-dot"></i> New Jersey, USA</li>
                         <li><i class="fas fa-phone-volume"></i> +1 (234) 567 89 10</li>
                         <li><i class="fas fa-envelope"></i> example@example.com</li>
                    </ul>
                    <div class="icons">
                        <div class="icon">
                            <i class="fab fa-facebook-f"></i>
                        </div>
                        <div class="icon">
                            <i class="fab fa-instagram"></i>
                        </div>
                        <div class="icon">
                            <i class="fab fa-twitter"></i>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <h3>Join Our Newsletter</h3>
                    <span>Subscribe to receive useful information.</span>
                    <div class="footer-input-group">
                        <input type="text" class="my-input" placeholder="Your Email Address" id="email" name="email">
                        <div class="my-button"> Subscribe <i class="fas fa-arrow-right-long"></i></div>
                    </div>
                </div>
                <div class="col-2">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam temporibus eum, adipisci maiores quidem dolor quos voluptate quam quae obcaecati explicabo cupiditate itaque impedit dolores consequuntur vero sapiente ea unde!
    
                </div>
                <div class="col-2">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam temporibus eum, adipisci maiores quidem dolor quos voluptate quam quae obcaecati explicabo cupiditate itaque impedit dolores consequuntur vero sapiente ea unde!
    
                </div>
                <div class="col-12">
                    <div class="text-center py-4">
                        &copy; 2024 Team#2 - Boolean
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
    @use '../styles/partial/variables' as *;
    @use '../styles/generals.scss';
    footer{
        background-color: $black;
        color: $grey;
        .logo{
            width: 80%;
        }
        .list-footer{
            list-style: none;
            li{
                margin: 10px 0;
                i{
                    font-size: 25px;
                    margin-right: 10px;
                }
            }
        }
        .icons{
            display: flex;
            gap: 10px;
            margin: 0 20px;
            .icon{
                border: 1px solid grey;
                padding: 5px 20px;
                i{
                    font-size: 30px;
                }
            }
        }
        .footer-input-group{
            margin-top: 20px;
            .my-input{
                width: 100%;
                border: none;
                padding: 20px;
            }
            .my-button{
                margin: 5px 0;
                padding: 20px;
                background-color: $white;
                color: $black;
                text-align: center;
            }
        }
    }
</style>