<template>
    <div>
        <h1 class="work-experience-title">Work Experience</h1>
        <div class="work-experience">
            <div class="work-experience-item" v-for="we in workExperience">
                <div class="we-card">
                    <div class="we-card-logo">
                        <img :src="we.logo" :alt="`${we.title} logo`">
                    </div>
                    <div class="we-card-content">
                        <div class="we-card-title">
                            {{ we.title}}
                        </div>
                        <div class="we-card-date">
                            {{ we.date}}
                        </div>
                        <div class="we-card-link">
                            <a target="_BLANK" :href="we.link">{{getLinkTitle(we.link)}}</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.work-experience-title {
    padding: 0 30px;
}

.work-experience {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    padding: 30px;
}

.work-experience-item {
    width: 50%;
}

.we-card {
    display: flex;
    align-items: center;
    background: #f1f1f1;
    box-shadow: 2px 2px 2px #f1f1f1;
    border-radius: 15px;
    width: 98%;
    margin: 10px 1%;
    padding: 15px;
    height:150px;
    cursor: pointer;
}

.we-card:hover {
    background: #e4f5e7;
}

.we-card-content {
    padding: 12px;
}

.we-card-title {
    font-weight: bold;
    font-size: 1.5rem;
}
.we-card-logo img{
    border-radius:100%
}

.we-card-link a {
    text-decoration: none;
}

@media screen and (max-width:768px) {

    .work-experience-title {
        padding: 0 12px;
        font-size: 1.2rem;
    }

    .work-experience {
        padding: 12px;
    }

    .work-experience-item {
        width: 100%;
    }

    .we-card {
        margin: 0;
        width: 100%;
        height:120px;
        margin-bottom: 10px;
    }

    .we-card-logo {
        width: 25%;
    }

    .we-card-logo img {
        width: 100%;
    }

    .we-card-title {
        font-size: 1rem;
    }

    .we-card-date,
    .we-card-link a {
        font-size: .7rem;
    }
}
</style>

<script setup>

const workExperience = [
    {
        logo: '/img/logo/getinclusive.png',
        title: 'Get Inclusive',
        date: 'Sep 2021 - Now',
        link: 'https://app.getinclusive.com'
    },
    {
        logo: '/img/logo/upwork.png',
        title: 'Freelancer on Upwork',
        date: 'Apr 2021 - Now',
        link: 'https://www.upwork.com/freelancers/~017cffa3dc7035c850'
    },
    {
        logo: '/img/logo/evordigi.png',
        title: 'Evordigi',
        date: 'Oct 2019 - Des 2019',
        link: 'https://evordigi.com'
    },
    {
        logo: '/img/logo/ponpescondong.png',
        title: 'Ponpes Condong',
        date: 'Oct 2019 - Feb 2020',
        link: 'https://ponpescondong.com'
    },
    {
        logo: '/img/logo/cvalphabet.png',
        title: 'CV Alphabet',
        date: 'Feb 2019 - Des 2020',
        link: 'https://alphabet.yucoding.com'
    },
    {
        logo: '/img/logo/kwarcabtasik.png',
        title: 'Kwarcab Tasik',
        date: 'Oct 2017 - Mar 2018',
        link: 'https://pramukakotatasik.or.id'
    }
]

const getLinkTitle = (link) => {
    if(link.length >= 28){
        return link.slice(0,28) + '..'
    }else{
        return link
    }
}
</script>