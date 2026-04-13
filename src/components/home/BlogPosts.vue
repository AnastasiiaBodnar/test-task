<script setup>
import runningImg from '@/assets/image/running.png'
import avatarImg from '@/assets/image/avatar.png'
import walksImg from '@/assets/image/walks.png'
import workoutImg from '@/assets/image/workout.png'
import fitnessImg from '@/assets/image/fitness.png'
import therapistImg from '@/assets/image/therapist.png'

const posts = [
    {
        id:1,
        title: 'Return to running after pregnancy – Is your body strong enough for running?',
        author: 'BY TILDA LOFTIN',
        avatar: avatarImg,
        date: 'JUNE 25, 2021',
        image: runningImg,
        large: true,
    },

       {
        id: 2,
        title: 'Stroller walks',
        date:'APRIL 21, 2021',
        image: walksImg,
        large: false,
    },

    {
        id: 3,
        title: 'Playground workout',
        date: 'MARCH 17, 2020',
        image: workoutImg,
        large: false,
    },

    {
        id: 4,
        title: 'Your Essential Fitness Gear for Each Trimester',
        date: 'FEBRUARY 21, 2021',
        image: fitnessImg,
        large: false,
    },

    {
        id: 5,
        title: 'What YOU could gain by working with a Woman’s Health Physical Therapist ',
        date: 'JANUARY 23, 2020',
        image: therapistImg,
        large: false,
    },
]

const largePosts = posts.filter(p => p.large)
const smallPosts = posts.filter(p => !p.large)
</script>

<template>
    <section class="blog">
        <div class="blog__container">

            <div class="blog__header">
                <h2 class="blog__title">Our blog posts</h2>
                <div class="blog__divider"></div>
            </div>

            <div class="blog__grid">
                <article 
                    v-for="post in largePosts"
                    :key="post.id"
                    class="blog__card blog__card--large">

                    <img :src="post.image" :alt="post.title" class="blog__card-img"/>

                    <div class="blog__caption">
                        <h4 class="blog__card-title">{{ post.title }}</h4>
                        <div class="blog__card-meta">
                            <img :src="post.avatar" :alt="post.author" class="blog__card-avatar">
                            <span class="blog__card-author">{{ post.author }}</span>
                            <span class="blog__card-date">{{ post.date }}</span>
                        </div> 
                    </div>
                </article>

                <div class="blog__small-grid"> 
                    <article
                        v-for="post in smallPosts"
                        :key="post.id"
                        class="blog__card blog__card--small"
                    >
                        <img :src="post.image" :alt="post.title" class="blog__card-img"/>

                        <div class="blog__caption">
                            <h5 class="blog__card-title">{{ post.title }}</h5>
                            <span class="blog__card-date">{{ post.date }}</span>
                        </div>
                    </article>
                </div>

            </div>

            <div class="blog__more">
                <span class="blog__more-text">Like what you see? View more</span>
                <button class="blog__more-btn">></button>
            </div>

        </div>
    </section>
</template>