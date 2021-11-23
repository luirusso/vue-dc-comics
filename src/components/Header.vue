<template>
  <header>
    <div class="container">
        <div class="main-logo">
          <img src="@/assets/dc-logo.png" alt="">
        </div>
        <div>
          <ul>
            <li v-for="link in navLinks" :key="link">
                <a href=""><strong> {{ link.link }} </strong></a>
            </li>
          </ul>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    data(){
        return{
            navLinks: [
                {
                    link: 'CHARACTERS'
                },
                {
                    link: 'COMICS'
                },
                {
                    link: 'MOVIES'
                },
                {
                    link: 'TV'
                },
                {
                    link: 'GAMES'
                },
                {
                    link: 'COLLECTIBLES'
                },
                {
                    link: 'VIDEOS'
                },
                {
                    link: 'FANS'
                },
                {
                    link: 'NEWS'
                },
                {
                    link: 'SHOP'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
header {
    height: 110px;
    font-size: 12px;

    div {
        height: 100%;
    }

    a {
        color: black;
        &:hover {
            color: #0282F9;
        }
    }

    .main-logo {
        display: flex;
        align-items: center;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    img {
        max-width: 80%;
    }

    ul {
        display: flex;
        list-style: none;
        height: 100%;
        align-content: center;
        justify-content: center;
        align-items: center;
    }

    li {
        height: 100%;
        display: flex;
        align-items: center;
        margin: 0 1rem;
        border-bottom: 4px solid transparent;
        transition: border-bottom 0.4s;
        &:hover,
        &:focus {
            border-bottom: 4px solid #0282F9;
        }

    }
}
</style>