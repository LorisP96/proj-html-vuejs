<template>
  <footer>
    <!-- BOOKING -->
    <div class="booking">
        <div class="book-cont flex">
            <div class="book-card flex">
                <div class="user-input">1 Person</div>
                <div class="card-child">FOR</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">11/29/2020</div>
                <div class="card-child">AT</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">1 Person</div>
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
                    <h5>SATURDAY</h5>
                    <span class="rest-info">Saturday 11am to midnight</span>
                </li>

                <li>
                    <h5>SUNDAY</h5>
                    <span class="rest-info">9:00 - 22:00</span>
                </li>
            </ul>
            <h3 class="about-child">THE DON PEPPE CREW FIRST AND FAREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA.</h3>
        </div>
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
    }
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
        padding-block: 100px;
        justify-content: center;

        &:first-child {
            background-color: $bg-black-1;
            padding-left: 70px;
            padding-right: 100px;

            .about-child {
                width: calc(100% / 3);

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
            }
        }

        &:last-child {
            background-image: url(../assets/img/footer-img-1.jpg);
            background-position: center;
        }
    }
}
</style>