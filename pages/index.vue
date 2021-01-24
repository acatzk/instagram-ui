<template>
  <div class="container mx-auto max-w-5xl px-0 sm:px-5 flex flex-row z-10">
    <div class="flex justify-center flex-row flex-1">

      <div class="w-screen sm:w-156 py-0.5 sm:py-7 overflow-x-auto">
        
        <div class="border border-gray-200 bg-white px-5 py-4 rounded-sm mb-0 sm:mb-6 ">
          <perfect-scrollbar>
            <ul class="inline-flex space-x-4">
              <li v-for="(story, i) in stories" :key="i" class="flex flex-col items-center space-y-0.5">
                <div class="p-0.5 rounded-full bg-gradient-to-tr from-yellow-400 to-fuchsia-600">
                  <a href="#" class="block rounded-full bg-white p-0.5 flex-shrink-0 w-14">
                    <img class="h-14 w-14 rounded-full" :src="story.avatar" alt="avatar" />
                  </a>
                </div>
                <a href="#" class="text-xs font-normal text-gray-800 tracking-tight">
                  {{ `${story.username.length >= 11 ? story.username.slice(0, 9) + '...' : story.username}` }}
                </a>
              </li>
            </ul>
          </perfect-scrollbar>
        </div>

        <div class="border-0 sm:border border-gray-200 bg-white rounded-sm">
          <!-- avatar & username -->
          <div class="flex items-center justify-between px-3 py-3">
            <div class="flex items-center space-x-2">
              <div class="flex-shrink-0">
                <Avatar src="https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/133848590_3512747115487394_1195628481626511236_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=Cz_qEggCw9QAX_L_EHl&tp=1&oh=ceca47bfac919297937982718033a8b7&oe=603601FC" className="w-7 h-7 rounded-full" story/>
              </div>
              <a href="#" class="text-sm font-medium">mchalvrz99</a>
            </div>
            <button class="focus:outline-none">
              <svg class="w-5 h-5 text-gray-800" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg>
            </button>
          </div>
          <!-- actual image -->
          <div class="flex-shrink-0">.
            <img class="object-cover" src="https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-15/e35/141499020_791412515118046_6265868457552450723_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&amp;_nc_cat=110&amp;_nc_ohc=AF0XflYT-1AAX8Tv9hA&amp;tp=1&amp;oh=a97d50cba3c419e1d8679c489c6d4296&amp;oe=6036A0BD" alt="post-image" />
          </div>
          <div class="space-y-2 pt-3">
            <!-- heart, comments & share -->
            <div class="flex items-center justify-between px-4">
              <div class="flex items-center space-x-4">
                <button class="focus:outline-none transition transform hover:scale-110 ease-in-out duration-75">
                  <svg class="w-6 h-6 fill-current text-red-500" viewBox="0 0 48 48"><path d="M34.6 3.1c-4.5 0-7.9 1.8-10.6 5.6-2.7-3.7-6.1-5.5-10.6-5.5C6 3.1 0 9.6 0 17.6c0 7.3 5.4 12 10.6 16.5.6.5 1.3 1.1 1.9 1.7l2.3 2c4.4 3.9 6.6 5.9 7.6 6.5.5.3 1.1.5 1.6.5s1.1-.2 1.6-.5c1-.6 2.8-2.2 7.8-6.8l2-1.8c.7-.6 1.3-1.2 2-1.7C42.7 29.6 48 25 48 17.6c0-8-6-14.5-13.4-14.5z"></path></svg>
                </button>
                <button class="focus:outline-none transition transform hover:scale-110 ease-in-out duration-75">
                  <svg class="w-6 h-6 fill-current" viewBox="0 0 48 48" width="24"><path clip-rule="evenodd" d="M47.5 46.1l-2.8-11c1.8-3.3 2.8-7.1 2.8-11.1C47.5 11 37 .5 24 .5S.5 11 .5 24 11 47.5 24 47.5c4 0 7.8-1 11.1-2.8l11 2.8c.8.2 1.6-.6 1.4-1.4zm-3-22.1c0 4-1 7-2.6 10-.2.4-.3.9-.2 1.4l2.1 8.4-8.3-2.1c-.5-.1-1-.1-1.4.2-1.8 1-5.2 2.6-10 2.6-11.4 0-20.6-9.2-20.6-20.5S12.7 3.5 24 3.5 44.5 12.7 44.5 24z" fill-rule="evenodd"></path></svg>
                </button>
                <button class="focus:outline-none transition transform hover:scale-110 ease-in-out duration-75">
                  <svg class="w-6 h-6 fill-current" viewBox="0 0 48 48" width="24"><path d="M47.8 3.8c-.3-.5-.8-.8-1.3-.8h-45C.9 3.1.3 3.5.1 4S0 5.2.4 5.7l15.9 15.6 5.5 22.6c.1.6.6 1 1.2 1.1h.2c.5 0 1-.3 1.3-.7l23.2-39c.4-.4.4-1 .1-1.5zM5.2 6.1h35.5L18 18.7 5.2 6.1zm18.7 33.6l-4.4-18.4L42.4 8.6 23.9 39.7z"></path></svg>
                </button>
              </div>
              <button class="focus:outline-none transition transform hover:scale-110 ease-in-out duration-75">
                <svg class="w-6 h-6 fill-current" viewBox="0 0 48 48" width="24"><path d="M43.5 48c-.4 0-.8-.2-1.1-.4L24 29 5.6 47.6c-.4.4-1.1.6-1.6.3-.6-.2-1-.8-1-1.4v-45C3 .7 3.7 0 4.5 0h39c.8 0 1.5.7 1.5 1.5v45c0 .6-.4 1.2-.9 1.4-.2.1-.4.1-.6.1zM24 26c.8 0 1.6.3 2.2.9l15.8 16V3H6v39.9l15.8-16c.6-.6 1.4-.9 2.2-.9z"></path></svg>
              </button>
            </div>
            <!-- person who reacted -->
            <div class="flex items-center space-x-1 px-4">
              <a href="#">
                <Avatar :className="`h-5 w-5 rounded-full`" src="https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/84064216_3082224618469048_6380949537762050048_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=px0ZpOnWawAAX_zhgTG&tp=1&oh=0866bb7fbcc4f3de4cb40dc938675d91&oe=60379698" />
              </a>
              <span class="text-sm font-normal tracking-tight">
                Liked by <a href="#" class="font-semibold">iamshaznaye</a> and <a href="#" class="font-semibold">54 others</a>
              </span>
            </div>
            <div class="space-y-1 flex flex-col border-b border-gray-100 px-4 pb-3">
              <span class="text-sm font-normal tracking-tight">
                <a href="#" class="font-semibold">mchalvrz99</a> Wine night
              </span>
              <a href="#" class="text-sm text-gray-400">View all 4 comments</a>
              <div class="flex items-center justify-between">
                <span class="text-sm font-normal tracking-tight">
                  <a href="#" class="font-semibold">nikkwooow</a> 
                  <a href="#" class="text-light text-blue-500">@mchalvrz99</a> <a href="#" class="text-light text-blue-500">@enzowwww</a> haaaaiii salamat ❤️
                </span>
                <button class="focus:outline-none">
                  <svg class="w-3 h-3" viewBox="0 0 48 48"><path d="M34.6 6.1c5.7 0 10.4 5.2 10.4 11.5 0 6.8-5.9 11-11.5 16S25 41.3 24 41.9c-1.1-.7-4.7-4-9.5-8.3-5.7-5-11.5-9.2-11.5-16C3 11.3 7.7 6.1 13.4 6.1c4.2 0 6.5 2 8.1 4.3 1.9 2.6 2.2 3.9 2.5 3.9.3 0 .6-1.3 2.5-3.9 1.6-2.3 3.9-4.3 8.1-4.3m0-3c-4.5 0-7.9 1.8-10.6 5.6-2.7-3.7-6.1-5.5-10.6-5.5C6 3.1 0 9.6 0 17.6c0 7.3 5.4 12 10.6 16.5.6.5 1.3 1.1 1.9 1.7l2.3 2c4.4 3.9 6.6 5.9 7.6 6.5.5.3 1.1.5 1.6.5.6 0 1.1-.2 1.6-.5 1-.6 2.8-2.2 7.8-6.8l2-1.8c.7-.6 1.3-1.2 2-1.7C42.7 29.6 48 25 48 17.6c0-8-6-14.5-13.4-14.5z"></path></svg>
                </button>
              </div>
              <div class="flex items-center justify-between">
                <span class="text-sm font-normal tracking-tight">
                  <a href="#" class="font-semibold">mchalvrz99</a> Hahaha kuya nikko 🤣🤦‍♀️
                </span>
                <button class="focus:outline-none">
                  <svg class="w-3 h-3" viewBox="0 0 48 48"><path d="M34.6 6.1c5.7 0 10.4 5.2 10.4 11.5 0 6.8-5.9 11-11.5 16S25 41.3 24 41.9c-1.1-.7-4.7-4-9.5-8.3-5.7-5-11.5-9.2-11.5-16C3 11.3 7.7 6.1 13.4 6.1c4.2 0 6.5 2 8.1 4.3 1.9 2.6 2.2 3.9 2.5 3.9.3 0 .6-1.3 2.5-3.9 1.6-2.3 3.9-4.3 8.1-4.3m0-3c-4.5 0-7.9 1.8-10.6 5.6-2.7-3.7-6.1-5.5-10.6-5.5C6 3.1 0 9.6 0 17.6c0 7.3 5.4 12 10.6 16.5.6.5 1.3 1.1 1.9 1.7l2.3 2c4.4 3.9 6.6 5.9 7.6 6.5.5.3 1.1.5 1.6.5.6 0 1.1-.2 1.6-.5 1-.6 2.8-2.2 7.8-6.8l2-1.8c.7-.6 1.3-1.2 2-1.7C42.7 29.6 48 25 48 17.6c0-8-6-14.5-13.4-14.5z"></path></svg>
                </button>
              </div>
              <a href="#" class="uppercase text-xxs text-gray-400">21 hours ago</a>
            </div>
          </div>
          <!-- form comments -->
          <form class="flex items-center justify-between overflow-hidden">
            <input type="text" placeholder="Add a comment..." class="w-full border-none focus:outline-none pl-4 py-4 text-sm">
            <button class="py-3 block focus:outline-none px-4 text-sm font-medium text-blue-500">
              Post
            </button>
          </form>
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
        <div>
          <ul>
            <li v-for="(user, i) in suggested" :key="i">
              <PopularUser :user="user"/>
            </li>
          </ul>
        </div>
        <div class="pt-6 space-y-1">
          <ul class="flex items-center space-x-1">
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">About</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Help</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Press API</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Jobs</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Privacy</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Terms</a>
              <span>&middot;</span>
            </li>
          </ul>
          <ul class="flex items-center space-x-1"> 
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Locations</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Top Accounts</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Hashtags</a>
              <span>&middot;</span>
            </li>
            <li class="text-xxs text-gray-300 flex items-center space-x-1">
              <a href="#">Language</a>
              <span>&middot;</span>
            </li>
          </ul>
        </div>
        <div class="pt-5 text-xxs uppercase text-gray-300">&copy; 2021 INSTAGRAM FROM FACEBOOK</div>
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
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/133848590_3512747115487394_1195628481626511236_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=Cz_qEggCw9QAX_L_EHl&tp=1&oh=ceca47bfac919297937982718033a8b7&oe=603601FC',
            username: 'mchalvrz99'
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/139362010_476642283726418_874369030295940692_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=DvVQ6VHgr6IAX_P3ukF&tp=1&oh=a11d0f6bf5729cd68d3ee7edd2fece57&oe=6037CC5B',
            username: 'kiraraang'
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/140086630_782418742368271_6187901265286384312_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=Q8LD9DXg4oMAX-cGGI9&tp=1&oh=9a879963a337361af2676710a30b8d43&oe=60351CBF',
            username: 'mimi04019ambot'
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/139167419_101047515265578_4781126747482455371_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=eNqoffAZG2cAX9kiiH1&tp=1&oh=917eb74c3768189fc73727d801e3ed1e&oe=6034CA69',
            username: 'jobebangs'
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/131891696_810886009471176_8585048192292460487_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=V2rzly5PEe0AX8t4PDp&tp=1&oh=30530ec1215c219cac1bbbb17477a590&oe=603588D9',
            username: 'stevenvansil'
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
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/121166489_988924188238321_59244122932831396_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=RbnhI7cxP5AAX_zi_lR&tp=1&oh=7e101115833afad2bf2e4eaaf32d712a&oe=60380D1E',
            username: 'jieselzamora',
            description: 'Followed by gilchristcalunia + 18 more',
            story: false
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/121625131_850324932404033_3098967443014584834_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=iI9Ojgv7WbMAX-aoVbW&tp=1&oh=df91866d031476eb118bc7e3b563441c&oe=603489C0',
            username: 'gons_norman',
            description: 'Follows you',
            story: false
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/59932746_756825654712847_2478677754539671552_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=ED2vJ7mAOakAX-Fo0aI&tp=1&oh=71512228cb1c52fb7d841d972e2679e9&oe=6037FD74',
            username: 'mickachii',
            description: 'Followed by kirararang + 9 more',
             story: false
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/118730814_649487335692615_2966814415371431857_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=UaW0Ojo035IAX_Vr-2v&tp=1&oh=185237f28d7e3687ff9de867f232a248&oe=6035446F',
            username: 'nylarimt',
            description: 'Followed by gilchristcalunia + 9 more',
            story: true
          },
          {
            avatar: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/139261613_1804527403053452_3888219302524999888_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=U-taTMeWjeoAX_aeKAA&tp=1&oh=7a831e026e1f7b2da902d42cf0e53ad8&oe=6036D60F',
            username: 'rrich05',
            description: 'Followed by angryboy19 + 4 more',
            story: false
          }
        ]
      }
    }
  }
</script>