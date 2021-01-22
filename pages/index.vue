<template>
  <div class="container mx-auto max-w-5xl px-0 sm:px-5 h-screen min-h-screen flex flex-row">
    <div class="flex flex-row flex-grow overflow-hidden">
      <div class="flex-grow py-0.5 sm:py-7">
        <div class="border border-gray-200 bg-white px-4 py-3 rounded-sm">
          <a href="#">
            romnic
          </a>
        </div>
      </div>
      <div class="w-96 flex-none hidden md:block px-6 mt-8">
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
          <li v-for="(user, i) in users" :key="i">
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
        users: [
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