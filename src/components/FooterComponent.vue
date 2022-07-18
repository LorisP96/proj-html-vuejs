<template>
  <footer>
    <!-- BOOKING -->
    <div class="booking">
        <div class="book-cont flex">
            <div class="book-card flex">
                <div class="user-input">1 Person <i class="fa-solid fa-user-group"></i></div>
                <div class="card-child">FOR</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">11/29/2020 <i class="fa-regular fa-calendar"></i></div>
                <div class="card-child">AT</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">7:00 PM <i class="fa-regular fa-bell"></i></div>
                <div class="card-child"></div>
            </div>
            <div class="book-card">
                <button>BOOK A TABLE</button>
            </div>
        </div>
    </div>

    <div class="about-us flex">
        <div class="about-cont flex">
            <ul class="about-child">
                <li><h4>FIND OUR RESTAURANTS</h4></li>
                <li v-for="restaurant, index in listRestaurants" :key="index">
                    <div class="rest-info">
                        <div>{{restaurant.road}}</div>
                        <div>{{restaurant.city}}</div>
                        <div>{{restaurant.number}}</div>
                    </div>
                </li>
            </ul>
            <ul class="about-child">
                <li><h4>WORKING HOURS</h4></li>
                <li>
                    <h5>MONDAY</h5>
                    <span class="rest-info closed">Kitchen Closed</span>
                </li>

                <li>
                    <h5>TUESDAY UNTIL FRIDAY</h5>
                    <span class="rest-info">9:00 - 22:00</span>
                </li>

                <li>
                    <h5>SATURDAY <span>*</span></h5>
                    <span class="rest-info">Saturday 11am to midnight</span>
                </li>

                <li>
                    <h5>SUNDAY</h5>
                    <span class="rest-info">9:00 - 22:00</span>
                </li>

                <li class="social">
                    <h5>FOLLOW US:</h5>
                    <i :class="socialIcon.Twitter"></i>
                    <i :class="socialIcon.Facebook"></i>
                    <i :class="socialIcon.Instagram"></i>
                    <i :class="socialIcon.LinkedIn"></i>
                </li>
            </ul>
            <h3 class="about-child">THE DON PEPPE CREW FIRST AND FAREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.</h3>
            <div class="created-by">
                <span>Created with <i class="fa-regular fa-heart"></i>. by</span> 
                <span> Loris Palazzo</span>
            </div>
            <div class="logo-v">
                <img src="../assets/img/h5-logo-divided-header-dark.png" alt="">
            </div>
        </div>
        <!-- Background Right -->
        <div class="about-cont"></div>
    </div>
  </footer>
</template>

<script>
export default {
    data() {
        return {
            listRestaurants: [
                {
                    road: '1614 E. Bell Rd #104.',
                    city: 'Salerno, AZ 85022',
                    number: '(602) 867-1010'
                },
                {
                    road: '204 E. Pizzetta Tommaso',
                    city: 'Sorrento, AZ 85022',
                    number: '(358) 867-1010'
                },
                {
                    road: 'Viale Puglia 54',
                    city: 'Torre Del Greco, AZ 85022',
                    number: '(358) 867-1010'
                },
                {
                    road: 'Corso Itali AA',
                    city: 'Naples, AZ 85022',
                    number: '(989) 867-1010'
                },
            ]
        }
    },
    props: {
        socialIcon: Object,
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.booking {
    background-image: url(../assets/img/h3-background-img-3.jpg);
    padding: 90px;
    background-position: -120px;
    margin-block: 8px;

    .book-cont {
        width: 60%;
        margin: 0 auto;
        line-height: 50px;

        .book-card {
            width: 25%;
            justify-content: space-between;
            color: $txt-white-1;
            position: relative;

            .card-child {
                width: 25%;
                text-align: center;
            }

            .user-input {
                height: 50px;
                padding-block: 10px;
                padding-inline: 20px;
                line-height: 30px;
                background-color: $fill-white;
                width: 75%;
                color: $txt-grey-3;
                font-size: 11px;
                border: 1px solid $border-black;

                i {
                    float: right;
                    display: inline-block;
                    height: 100%;
                    line-height: 30px;
                    color: $txt-gold-2;
                    font-size: 16px;
                }
            }

            button {
                width: 75%;
                height: 100%;
                display: block;
                font-family: inherit;
                letter-spacing: 2px;
                font-size: 11px;
                background-color: $bg-red-3;
                color: inherit;
                border: 0;
            }
        }
    }
}

.about-us {

    .about-cont {
        width: 50%;
        padding-top: 100px;
        justify-content: center;

        &:first-child {
            background-color: $bg-black-1;
            padding-left: 70px;
            padding-right: 100px;
            flex-wrap: wrap;
            position: relative;

            .about-child {
                width: calc(100% / 3);
                padding-bottom: 120px;

                &:nth-child(2) {
                    padding-left: 10px;
                }

                &:last-child {
                font-size: 20px;
                color: $txt-white-1;
                padding-left: 30px;
                padding-top: 5px;
                
                }

                li {
                    padding-block: 7px;

                    h4 {
                        color: $txt-gold-2;
                        font-size: 15px;
                        padding-bottom: 8px;
                    }

                    h5 {
                        color: $txt-gold-2;
                        font-size: 11.5px;

                        span {
                            color: $txt-red-1;
                            font-size: 16px;
                            font-weight: 400;
                        }
                    }

                    .rest-info {
                    color: $txt-grey-4;
                    font-size: 12px;
                    line-height: 20px;
                    letter-spacing: 2px;
                    }

                    .closed {
                        color: $txt-red-2;
                    }
                }
                
                .social {
                    padding-top: 20px;

                    h5 {
                        display: inline-block;
                    }

                    i {
                        display: inline-block;
                        font-size: 10px;
                        color: $txt-white-1;
                        padding-inline: 5px;
                    }
                }
            }

            h3 {
                color: $txt-white-1;
            }

            .created-by {
                width: 100%;
                font-size: 11px;
                padding-bottom: 60px;
                
                span {
                    color: $txt-gold-2;

                    &:last-child {
                        color: $txt-green;
                    }

                    i {
                        display: inline-block;
                        padding-inline: 2px;
                    }
                }
            }

            .logo-v {
                position: absolute;
                height: 130px;
                width: 130px;
                bottom: 0px;
                right: 50px;
            }
        }

        &:last-child {
            background-image: url(../assets/img/footer-img-1.jpg);
            background-position: center;
        }
    }
}
</style>