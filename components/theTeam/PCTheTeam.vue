<template>
    <div style="background-color: #FDF9F3;">
        <PCHeader :is-dark="true"/>
        <div style="height: 237px;"></div>
        <section :class="$style.container_1">
            <div style="width: 40%; flex: 4; margin: 0 auto;">
                <p class="page_title" style="font-size: 110px;">The</p>
                <p class="page_title" style="font-weight: 700; font-size: 110px;">Team</p>
            </div>
            <p :class="$style.description" style="flex: 6">
                At Konpanion we are proud to be part of a multidisciplinary team with skillsets ranging from fashion, linguistics, robotics and machine learning. We believe this allows Konpanion to be a place for fertile imaginative thinking, an essential skill to invent companion robots for the real world. We are always looking for new talents to join our team, feel free to get in touch! 
            </p>
        </section>


        <div style="height: 250px;"></div>
        <section :class="$style.container_2">

            <team-member 
                v-for="founder in founders"
                :key="founder.name"
                :name="founder.name"
                :bio="founder.bio"
                :email="founder.email"
                :image="founder.image"
                :role="founder.role"
                style="flex: 1; width: 100%;"/>
        </section>

        <div style="height: 110px;"></div>

        <section :class="$style.container_3">
            <s-team-member
                v-for="team in teams"
                :key="team.name"
                :name="team.name"
                :image="team.image"
                :role="team.role"
                style="flex: 1; width: 100%;"/>
        </section>

        <div style="height: 110px;"></div>

        <p :class="$style.advisors">OUR ADVISORS</p>

        <section :class="$style.container_4">
            <s-team-member
                v-for="advisor in advisors"
                :key="advisor.name"
                :name="advisor.name"
                :image="advisor.image"
                :role="advisor.role"
                />
        </section>

        <div style="height: 100px;"></div>
        <img src="../../assets/images/footer.png" alt="" width="100%">
    </div>
</template>

<script>
import {advisors, coFounders, teamMembers} from '../../const/constants.js';
import PCHeader from '../headers/PCHeader.vue';
import STeamMember from './STeamMember.vue';
import TeamMember from './TeamMember.vue';

export default {
name: 'PCTheTeam',
components: { TeamMember, STeamMember, PCHeader },
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
};
</script>

<style module>
.container_1 {
    display: flex;
    align-items: start;
    padding: 250px 15% 0 15%;
}


.description {
    color: #000;
    font-family: Spartan;
    font-size: 25px;
    font-style: normal;
    font-weight: 200;
    line-height: 37px; /* 148% */
}

.container_2 {
    display: flex;
    justify-content: space-evenly;
    gap: 7vw;
    padding: 0 10%;

}

.container_3 {
    display: flex;
    justify-content: space-evenly;
    gap: 7vw;
    padding: 0 10%;
}

.container_4 {
    display: grid;
    /* 3 columns */
    grid-template-columns: repeat(3, 1fr);
    gap: 5vw;
    padding: 0 19%;
}

.advisors {
    color: #282B46;
    text-align: center;
    font-family: Spartan;
    font-size: 42px;
    font-style: normal;
    font-weight: 400;
    line-height: 60px; /* 142.857% */
    letter-spacing: 5.04px;
}
</style>