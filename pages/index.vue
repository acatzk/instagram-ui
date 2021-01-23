<template>
  <div class="container mx-auto max-w-5xl px-0 sm:px-5 flex flex-row z-10">
    <div class="flex justify-center flex-row flex-1">

      <div class="w-screen sm:w-156 py-0.5 sm:py-7 overflow-x-auto">
        <div class="border border-gray-200 bg-white px-5 py-4 rounded-sm">
          <perfect-scrollbar>
            <ul class="inline-flex space-x-4">
              <li v-for="(story, i) in stories" :key="i" class="flex flex-col items-center space-y-0.5">
                <div class="p-0.5 rounded-full bg-gradient-to-tr from-yellow-400 to-fuchsia-600">
                  <a href="#" class="block rounded-full bg-white p-0.5 flex-shrink-0 w-14">
                    <img class="h-14 w-14 rounded-full" :src="story.avatar" alt="avatar" />
                  </a>
                </div>
                <a href="#" class="text-xs font-normal text-gray-800 tracking-tight">{{ story.username }}</a>
              </li>
            </ul>
          </perfect-scrollbar>
        </div>
      </div>

      <div class="flex-grow hidden lg:block px-6 mt-8">
        <div class="flex items-center justify-between py-4">
          <div class="flex items-center space-x-4">
            <div class="flex-shrink-0">
              <Avatar className="w-14 h-14 rounded-full" story/>
            </div>
            <div class="flex flex-col">
              <a href="#" class="text-sm font-semibold">h.moves</a>
              <span class="text-sm text-gray-400">Hokage Moves</span>
            </div>
          </div>
          <a href="#" class="text-xs font-medium text-blue-500">Switch</a>
        </div>
        <div class="flex items-center justify-between">
          <span class="text-sm font-semibold text-gray-400">Suggestions For You</span>
          <a href="#" class="text-sm font-medium tracking-tight">See all</a>
        </div>
        <ul>
          <li v-for="(user, i) in suggested" :key="i">
            <PopularUser :user="user"/>
          </li>
        </ul>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    head: {
      title: 'Instagram'
    },
    components: {
      PopularUser: () => import('~/components/PopularUser'),
      Avatar: () => import('~/components/Avatar')
    },
    data () {
      return {
        stories: [
          {
            avatar: 'https://uifaces.co/our-content/donated/vIqzOHXj.jpg',
            username: 'bigbro23'
          },
          {
            avatar: 'https://manskkp.lv/assets/images/users/4.jpg',
            username: 'sister27'
          },
          {
            avatar: 'https://cdn.vox-cdn.com/thumbor/Zz5I08Bvcjs9j_AbBK_L4ZoWnbE=/1400x0/filters:no_upscale()/cdn.vox-cdn.com/uploads/chorus_asset/file/19216619/000024.jpg',
            username: 'abegail23'
          },
          {
            avatar: 'https://pbs.twimg.com/profile_images/1001332003474567169/vDCiE04W_400x400.jpg',
            username: 'laisa2'
          },
          {
            avatar: 'https://manskkp.lv/assets/images/users/6.jpg',
            username: 'georgy23'
          },
          {
            avatar: 'https://lokjat.com/wp-content/uploads/2015/03/team-member-5.jpg',
            username: 'nerby'
          },
          {
            avatar: 'https://bootstrap.gallery/everest-v3//img/user1.jpg',
            username: 'blackbeard'
          },
          {
            avatar: 'https://qph.fs.quoracdn.net/main-qimg-6291c3a117fc230c82785148baef7eed',
            username: 'gayle2'
          },
          {
            avatar: 'https://pbs.twimg.com/profile_images/1001332003474567169/vDCiE04W_400x400.jpg',
            username: 'laisa2'
          },
          {
            avatar: 'https://manskkp.lv/assets/images/users/6.jpg',
            username: 'georgy23'
          },
          {
            avatar: 'https://lokjat.com/wp-content/uploads/2015/03/team-member-5.jpg',
            username: 'nerby'
          },
          {
            avatar: 'https://bootstrap.gallery/everest-v3//img/user1.jpg',
            username: 'blackbeard'
          },
          {
            avatar: 'https://qph.fs.quoracdn.net/main-qimg-6291c3a117fc230c82785148baef7eed',
            username: 'gayle2'
          }
        ],
        suggested: [
          {
            avatar: 'https://www.gravatar.com/avatar/205e460b479e2e5b48aec07710c08d50?s=200',
            username: 'nylarimt',
            story: true
          },
          {
            avatar: 'https://uifaces.co/our-content/donated/vIqzOHXj.jpg',
            username: 'vnthony.leodones',
            description: 'Popular',
            story: false
          },
          {
            avatar: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_d3SP2vKOeGFVESn5rk6xnPiQ0naW2e-ldA&usqp=CAU',
            username: 'abhiandniyu',
            description: 'Popular',
             story: true
          },
          {
            avatar: 'https://dt2sdf0db8zob.cloudfront.net/wp-content/uploads/2019/12/9-Best-Online-Avatars-and-How-to-Make-Your-Own-for-Free-image1-5.png',
            username: 'rrich05',
            description: 'Suggested for you',
            story: false
          },
          {
            avatar: 'https://leadslive.io/wp-content/uploads/2017/05/Miniclip-8-Ball-Pool-Avatar-11.png',
            username: 'hey.itsnahmae',
            description: 'Suggested for you',
            story: false
          }
        ]
      }
    }
  }
</script>