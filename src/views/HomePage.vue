<script setup>
import BlogPosts from '@/components/home/BlogPosts.vue';
import CtaBanner from '@/components/home/CtaBanner.vue';
import HeroSection from '@/components/home/HeroSection.vue';
import HowItWorks from '@/components/home/HowItWorks.vue';
import PregnancyStages from '@/components/home/PregnancyStages.vue';

import runningImg from '@/assets/image/running.png'
import avatarImg from '@/assets/image/avatar.png'
import walksImg from '@/assets/image/walks.png'
import workoutImg from '@/assets/image/workout.png'
import fitnessImg from '@/assets/image/fitness.png'
import therapistImg from '@/assets/image/therapist.png'

const posts = [
  {
    id: 1,
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
    date: 'APRIL 21, 2021',
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
</script>

<template>
  <div>
    <HeroSection />
    <HowItWorks />
    <PregnancyStages />
    <BlogPosts :posts="posts" />
    <CtaBanner />
  </div>
</template>