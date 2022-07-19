<template>
    <section class="teams flex">
        <div class="team-card">
            <img src="../assets/img/h1-team-1a-700x700.jpg" alt="team member 1">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div class="social-team">
                    <i :class="socialIcon.Instagram"></i>
                    <i :class="socialIcon.Twitter"></i>
                    <i :class="socialIcon.Facebook"></i>
                </div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-2a.jpg" alt="team member 2">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div class="social-team">
                    <i :class="socialIcon.Instagram"></i>
                    <i :class="socialIcon.Twitter"></i>
                    <i :class="socialIcon.Facebook"></i>
                </div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-4a.jpg" alt="team member 3">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div class="social-team">
                    <i :class="socialIcon.Instagram"></i>
                    <i :class="socialIcon.Twitter"></i>
                    <i :class="socialIcon.Facebook"></i>
                </div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-3a.jpg" alt="team member 4">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div class="social-team">
                    <i :class="socialIcon.Instagram"></i>
                    <i :class="socialIcon.Twitter"></i>
                    <i :class="socialIcon.Facebook"></i>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        socialIcon: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.teams {
    padding-block: 8px;

    .team-card {
        width: calc(100% / 4);
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;

        &::before {
            content: "";
            background-image: url('https://i.pinimg.com/originals/be/f3/86/bef386ecd3ddea8424067f7c0c2048c5.png');
            background-size: cover;
            position: absolute;
            top: 0px;
            right: 0px;
            bottom: 0px;
            left: 0px;
            opacity: 0;
        }

        .info-card {
            width: 88%;
            height: 88%;
            background-color: $bg-red-3;
            display: none;
            // border: 25px solid $border-white-1;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: $txt-white-1;
            position: relative;

            h3 {
                font-size: 25px;
                font-weight: 400;
            }

            .job {
                font-size: 15px;
                font-weight: 300;
                padding-bottom: 15px;
            }

            .social-team {
                i {
                    display: inline-block;
                    padding-inline: 5px;
                }
            }
        }

        &:hover img {
            display: none;
        }

        &:hover div {
            display: flex;
        }

        &:hover::before {
            opacity: 0.25;
        }
    }
}
</style>