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

<style scoped>

.blog {
    padding: 30px 0 60px 0;
}

.blog__container {
    max-width: 1200px;
    margin: 0 auto;
}

.blog__header {
    text-align: center;
    margin-bottom: 40px;
}

.blog__title {
    font-weight: 700;
    font-size: 50px;
    line-height: 100%;
    color: var(--color-dark-text);
}

.blog__divider {
    width: 45px;
    height: 3px;
    background-color: var(--color-divider);
    margin: 20px auto 0px auto;
}

.blog__grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
    margin-bottom: 16px;
}

.blog__small-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
}

.blog__card {
    position: relative;
    border-radius: 14px;
    overflow: hidden;
    isolation: isolate;
}

.blog__card--large {
    height: 600px;
}

.blog__card--small {
    height: 283px;
}

.blog__card-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    display: block;
}

.blog__caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 20px;
    color: var(--color-white);
}

.blog__card--large .blog__card-title {
    font-size: 32px;
    font-weight: 700;
    line-height: 100%;
    margin: 0 0 8px 0;
}

.blog__card--small .blog__card-title {
    font-size: 24px;
    font-weight: 700;
    line-height: 100%;
    margin: 0 0 6px 0;
}

.blog__card-meta {
    display: flex;
    align-items: center;
    gap: 12px;
}

.blog__card-avatar {
    height: 30px;
}

.blog__card-author {
    font-weight: 400;
    font-size: 16px;
    line-height: 28px;
    padding-right: 20px;
}

.blog__card-date {
    font-weight: 400;
    font-size: 16px;
    line-height: 28px;
}

.blog__more {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;
    padding-top: 20px;
}

.blog__more-text {
    font-weight: 400;
    font-size: 24px;
    line-height: 160%;
}

.blog__more-btn {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: var(--color-primary);
    color: var(--color-white);
    border: none;
    font-size: 20px;
    cursor: pointer;
}

@media (max-width: 1260px) {
  .blog__container {
    padding: 0 60px;
  }
  .blog__title {
    font-size: 42px; 
  }
  .blog__card--large {
    height: 500px; 
  }
  .blog__card--small {
    height: 240px; 
  }
  .blog__card--large .blog__card-title {
    font-size: 28px;
  }
  .blog__card--small .blog__card-title {
    font-size: 18px;
  }

  .blog__card-avatar {
    height: 25px;
}
}

@media (max-width: 768px) {
  .blog__container {
    padding: 0 24px;
  }
  .blog__grid, .blog__small-grid {
    grid-template-columns: 1fr;
  }
  .blog__card--large,
  .blog__card--small {
    height: 350px;
  }
  .blog__card--large .blog__card-title,
  .blog__card--small .blog__card-title {
    font-size: 24px;
  }
}

@media (max-width: 320px) {
  .blog__container {
    padding: 0 16px;
  }
  .blog__title { font-size: 36px; }
  .blog__card--large,
  .blog__card--small { 
    height: 240px; 
  }
  .blog__card--large .blog__card-title,
  .blog__card--small .blog__card-title {
    font-size: 20px;
  }
}
</style>