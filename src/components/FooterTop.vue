<script>
export default {
  data() {
    return {
      dcComicsLists: [
        {
          text: 'Characters',
          url: '#',
        },
        {
          text: 'Comics',
          url: '#',
        },
        {
          text: 'Movies',
          url: '#',
        },
        {
          text: 'TV',
          url: '#',
        },
        {
          text: 'Games',
          url: '#',
        },
        {
          text: 'Collectibles',
          url: '#',
        },
        {
          text: 'Videos',
          url: '#',
        },
        {
          text: 'Fans',
          url: '#',
        },
        {
          text: 'News',
          url: '#',
        }
      ],
      shopLists: [
        {
          text: 'Shop DC',
          url: '#',
        },
        {
          text: 'Shop DC Collectibles',
          url: '#',
        }
      ],
      dcLists: [
        {
          text: 'Terms Of Use',
          url: '#',
        },
        {
          text: 'Privacy police (New)',
          url: '#',
        },
        {
          text: 'Ad Choices',
          url: '#',
        },
        {
          text: 'Advertising',
          url: '#',
        },
        {
          text: 'Jobs',
          url: '#',
        },
        {
          text: 'Subscriptions',
          url: '#',
        },
        {
          text: 'Talent Workshops',
          url: '#',
        },
        {
          text: 'CPSC Certificates',
          url: '#',
        },
        {
          text: 'Ratings',
          url: '#',
        },
        {
          text: 'Shop Help',
          url: '#',
        },
        {
          text: 'Contact Us',
          url: '#',
        }
      ],
      siteLists: [
        {
          text: 'DC',
          url: '#',
        },
        {
          text: 'MAD Magazine',
          url: '#',
        },
        {
          text: 'DC Kids',
          url: '#',
        },
        {
          text: 'DC Universe',
          url: '#',
        },
        {
          text: 'DC Power Visa',
          url: '#',
        },
      ],
    }
  },
}
</script>

<template>
  <div class="bg-top-foot">
    <div class="container footer-top">
      <div class="left">
        <nav id="dc-comics">
          <h3>DC COMICS</h3>
          <ul>
            <li v-for="item in dcComicsLists"><a :href="item.url">{{ item.text }}</a></li>
          </ul>
        </nav>
        <nav id="shop">
          <h3>SHOP</h3>
          <li v-for="item in shopLists"><a :href="item.url">{{ item.text }}</a></li>
        </nav>
      </div>
      <div>

        <nav id="dc" class="center">
          <h3>DC</h3>
          <li v-for="item in dcLists"><a :href="item.url">{{ item.text }}</a></li>
        </nav>
      </div>

      <div>

        <nav id="sites" class="right">
          <h3>SITES</h3>
          <li v-for="item in siteLists"><a :href="item.url">{{ item.text }}</a></li>
        </nav>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bg-top-foot {
  height: calc(100vh - 480px);
  background-image: url('../assets/img/dc-logo-bg.png'), url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat, no-repeat;
  background-size: 600px, cover;
  background-position: center;
  background-position-x: 1000px, 0;
}

.footer-top {
  display: flex;
  padding-top: 45px;
  gap: 40px;


  h3 {
    margin: 10px 0;
  }

  li {
    font-size: 0.8rem;
    margin-bottom: 5px;

    &:hover {
      text-decoration: underline;
    }
  }
}
</style>