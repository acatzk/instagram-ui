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
          <div class="flex items-center justify-between px-3 py-3">
            <div class="flex items-center space-x-2">
              <div class="flex-shrink-0">
                <Avatar src="https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/133848590_3512747115487394_1195628481626511236_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=Cz_qEggCw9QAX_L_EHl&tp=1&oh=ceca47bfac919297937982718033a8b7&oe=603601FC" className="w-7 h-7 rounded-full" story/>
              </div>
              <span class="text-sm font-medium">mchalvrz99</span>
            </div>
            <button class="focus:outline-none">
              <svg class="w-5 h-5 text-gray-800" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg>
            </button>
          </div>
          <div class="flex-shrink-0">
            <img class="object-cover" src="https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-15/e35/141499020_791412515118046_6265868457552450723_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&amp;_nc_cat=110&amp;_nc_ohc=AF0XflYT-1AAX8Tv9hA&amp;tp=1&amp;oh=a97d50cba3c419e1d8679c489c6d4296&amp;oe=6036A0BD" alt="post-image" />
          </div>
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