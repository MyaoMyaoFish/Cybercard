<script lang='ts'>
  import Icon from 'svelte-awesome'
  import { envelope, github, qq, share, steam, telegram, twitter, weibo } from 'svelte-awesome/icons'
  import { faBilibili as bilibili, faTiktok as tiktok } from '@fortawesome/free-brands-svg-icons'

  interface Social {
    text: string;
    icon: any;
    link: string;
  }

  const socials: Social[] = [
    { text: '2300201323', icon: qq, link: 'https://qm.qq.com/cgi-bin/qm/qr?k=vHDuPj4mXJzEMonxat8r1fTpkmX_71bg' },
    { text: '不会游泳淼淼鱼', icon: bilibili, link: 'https://space.bilibili.com/552011175' },
    { text: '@MyaoMyaoFish', icon: twitter, link: 'https://twitter.com/MyaoMyaoFish' },
    { text: '@MyaoMyaoFish', icon: github, link: 'https://github.com/MyaoMyaoFish' },
    { text: 'jimyao@outlook.com', icon: envelope, link: 'mailto:jimyao@outlook.com' },
    { text: '感谢 ShellWen 对本页面的贡献', icon: share, link: 'https://blog.gfmc.top/' },
  ]
</script>

<div class='w-full h-[400px] flex-1 flex flex-col justify-between p-4'>
  <div class='flex flex-col'>
    {#each socials as social}
      <a class='link' href={social.link} rel='noopener noreferrer' target='_blank'>
        <Icon class='inline-block' data={social.icon} />
        {social.text}
      </a>
    {/each}
  </div>
  <div class='relative'>
    <img alt='' class='absolute bottom-0 right-0 translate-y-[35px] translate-x-[15px] w-32'
         src='/image/tx2.png' />
  </div>
</div>

<style>
  .link {
    @apply w-fit;
  }
</style>
