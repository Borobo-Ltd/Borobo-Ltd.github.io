<template>
    <div style="background-color: #FDF9F3;">
        <m-header />
        <div :class="$style.wrapper">
            <section :class="$style.container_1">
                <p class="page_title">The</p>
                <p class="page_title" style="font-weight: 700;">Team</p>

                <p :class="$style.description">
                    At Konpanion we are proud to be part of a multidisciplinary team with skillsets ranging from fashion, linguistics, robotics and machine learning. We believe this allows Konpanion to be a place for fertile imaginative thinking, an essential skill to create companion robots for the real world. 
                    <br><br>
                    We are always looking for new talents to join our team, feel free to get in touch!
                </p>
            </section>
            <section :class="$style.container_1">
                <team-member 
                    v-for="founder in founders"
                    :key="founder.name"
                    :name="founder.name"
                    :role="founder.role"
                    :bio="founder.bio"
                    :email="founder.email"
                    :image="founder.image"
                    gap="20px"/>
            </section>

            <section :class="$style.container_2">
                <s-team-member
                    v-for="team in teams"
                    :key="team.name"
                    :name="team.name"
                    :role="team.role"
                    :image="team.image"
                    name-size="11px"
                    role-size="10px"
                    role-height="14px"
                    top="50px"
                    />

            </section>

            <p :class="$style.advisors">OUR ADVISORS</p>

            <section :class="$style.container_2">
                <s-team-member
                    v-for="advisor in advisors"
                    :key="advisor.name"
                    :name="advisor.name"
                    :role="advisor.role"
                    :image="advisor.image"
                    name-size="11px"
                    role-size="10px"
                    role-height="14px"
                    top="50px"
                    />

            </section>

        </div>

        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import MHeader from '../headers/MHeader.vue';
import {advisors, coFounders, teamMembers} from '../../const/constants.js';
import STeamMember from './STeamMember.vue';
import TeamMember from './TeamMember.vue';

export default {
    name: 'MTheTeam',
    components: {
        MHeader,
        TeamMember,
        STeamMember,
    },
    data() {
        const foundersData = coFounders;
        const teamsData = teamMembers;
        const advisorData = advisors;

        

        return {
            founders: foundersData,
            teams: teamsData,
            advisors: advisorData,
        }
    }
}
</script>

<style lang="css" module>

.container_1 {
    padding: 0 10%;
}

.container_2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5vw;
    padding: 0 5%;
}

.description {
    color: #282B46;
    font-family: Spartan;
    font-size: 16px;
    font-style: normal;
    font-weight: 300;
    line-height: 30px; /* 187.5% */
    padding-top: 50px;
}

.advisors {
    color: #282B46;
    text-align: center;
    font-family: Spartan;
    font-size: 22px;
    font-style: normal;
    font-weight: 700;
    line-height: 33px; /* 150% */
    letter-spacing: 2.64px;
    padding-top: 50px;
}

</style>