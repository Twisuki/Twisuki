<img src="src/round.png" width="250px" height="250px" align="right" />

<br />

<picture>
	<source media="(prefers-color-scheme: dark)" srcset="src/titleType.svg" />
	<source media="(prefers-color-scheme: light)" srcset="src/titleType-light.svg" />
	<img height="50px" src="src/titleType.svg" />
</picture>

<br />

<picture>
	<source media="(prefers-color-scheme: dark)" srcset="src/titleType-en.svg" />
	<source media="(prefers-color-scheme: light)" srcset="src/titleType-en-light.svg" />
	<img height="40px" src="src/titleType-en.svg" />
</picture>

<br/>

![](https://github-readme-activity-graph.vercel.app/graph?username=Twisuki&theme=xcode&hide_border=true)

## 个人简介 Profile

[![Steam](https://img.shields.io/badge/Su__Yang__233-black.svg?logo=Steam)](https://steamcommunity.com/profiles/76561199387291268/)
[![Minecraft](https://img.shields.io/badge/Minecraft-Nya__Twisuki-green.svg?labelColor=green&color=yellowgreen)](https://namemc.com/profile/Nya_Twisuki)
[![Bilibili](https://img.shields.io/badge/Nya__Twisuki-pink.svg?logo=Bilibili)](https://space.bilibili.com/317707977)

![Name](https://img.shields.io/badge/Nya__Twisuki-SuYang233-blue)
![University](https://img.shields.io/badge/AI-HNU-red)
![Gender](https://img.shields.io/badge/Agender-Trans-aqua)


- 我是 Twisuki, 中文名苏阳, 来自辽宁.
    - I'm Twisuki, Su_Yang in Chinese, from Liaoning Province, China.
- 就读于湖南大学, 学习人工智能.
    - Learning AI in HNU.
- 现在在 bilibili 担任前端实习生.
    - Currently, a front-end intern at bilibili.

## 开发概况 Development

![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)

![Vue](https://img.shields.io/badge/-Vue-4FC08D?logo=Vue.js&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?logo=React&logoColor=white)
![Nuxt](https://img.shields.io/badge/-Nuxt-00DC82?logo=Nuxt&logoColor=white)
![Next](https://img.shields.io/badge/-Next-000000?logo=Next.js&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?logo=FastAPI&logoColor=white)

- 精通 Vue, React 和 web vanilla 前端.
    - Proficient in Vue, React, and vanilla web frontend.
- 正在学习后端, 主要是 Python 和 Rust.
    - Learning backend now, mainly Python and Rust.
- 目前在湖南大学某学生组织工作, 运维一个 React / Taro 小程序.
    - Currently working in a student organization at Hunan University, maintaining a React/Taro mini program.

<div> 
  <!-- Repo info cards - https://github.com/anuraghazra/github-readme-stats -->
  <!-- Small repo cards (fork) - https://github.com/DenverCoder1/github-readme-stats -->
  <!-- 感谢上面两位开发者. / Thanks to the two developers above. -->
  
  <p align="left">
    <a href="https://github.com/qnxg/weihuda_weapp_tsumiki">
      <img width="278" src="https://denvercoder1-github-readme-stats.vercel.app/api/pin/?username=qnxg&repo=weihuda_weapp_tsumiki" alt="weihuda_weapp_tsumiki">
    </a>
    <a href="https://github.com/Twisuki/homepage">
      <img width="278" src="https://denvercoder1-github-readme-stats.vercel.app/api/pin/?username=Twisuki&repo=homepage" alt="homepage">
    </a>
    <a href="https://github.com/Twisuki/ohday">
      <img width="278" src="https://denvercoder1-github-readme-stats.vercel.app/api/pin/?username=Twisuki&repo=ohday" alt="ohday">
    </a>
    <a href="https://github.com/Twisuki/HMOIndex">
      <img width="278" src="https://denvercoder1-github-readme-stats.vercel.app/api/pin/?username=Twisuki&repo=HMOIndex" alt="HMOIndex">
    </a>
  </p>
</div>

## 近期动态 Recent Activity
<!--WAKA_BLOG_SYNC_START-->
<!--CUSTOM_WAKA_START-->
const formatTime = (seconds) => {
  const h = Math.floor(seconds / 3600)
  const m = Math.floor((seconds % 3600) / 60)
  const hu = h === 1 ? 'hr' : 'hrs'
  const mu = m === 1 ? 'min' : 'mins'
  return encodeURIComponent(
    `${h.toLocaleString('en-US')} ${hu} ${m} ${mu}`
  )
}

const formatLines = (total) => {
  const v = (total / 1000).toLocaleString('en-US', { minimumFractionDigits: 2, maximumFractionDigits: 2 })
  return encodeURIComponent(`${v}k`)
}

const codeTimeWeek = formatTime(waka.week?.time ?? 0)
const codeTimeAll = formatTime(waka.all?.time ?? 0)
const linesOfCodeWeek = formatLines((waka.week?.addition?.total ?? 0) + (waka.week?.deletion?.total ?? 0))
const linesOfCodeAll = formatLines((waka.all?.addition?.total ?? 0) + (waka.all?.deletion?.total ?? 0))

const renderList = (items) => {
  if (!items) return ''
  const total = items.reduce((s, i) => s + i.time, 0)
  return items.slice(0, 5).map(item => {
    const h = Math.floor(item.time / 3600)
    const m = Math.floor((item.time % 3600) / 60)
    const hu = h === 1 ? 'hr' : 'hrs'
    const mu = m === 1 ? 'min' : 'mins'
    const time = h > 0 ? `${h} ${hu} ${m} ${mu}` : `${m} ${mu}`
    const percent = total > 0 ? (item.time / total) * 100 : 0
    const filled = Math.round(percent / 100 * 25)
    const bar = '█'.repeat(filled) + '░'.repeat(25 - filled)
    return `- ${item.name.padEnd(22)}${time.padEnd(17)}${bar}${(percent.toFixed(2) + ' %').padStart(8)}`
  }).join('\n')
}

const languagesText = renderList(languages.week)
const editorsText = renderList(editors.week)

const lastUpdated = new Date().toISOString().slice(0, 19).replace('T', ' ')
<!--CUSTOM_WAKA_END-->

This Week:
![Code Time](https://img.shields.io/badge/Code%20Time-{codeTimeWeek}-blue?style=flat)
![Lines of code](https://img.shields.io/badge/Lines%20of%20Code-{linesOfCodeWeek}-aqua?style=flat)

From Hello World:
![Code Time](https://img.shields.io/badge/Code%20Time-{codeTimeAll}-green?style=flat)
![Lines of code](https://img.shields.io/badge/Lines%20of%20Code-{linesOfCodeAll}-lime?style=flat)

```text
Top Languages This Week:

{languagesText}

And Top Editors:

{editorsText}
```

Last Updated on {lastUpdated} UTC
<!--WAKA_BLOG_SYNC_END-->

powered by [![Twisuki/custom_waka_readme](https://img.shields.io/badge/Twisuki-custom_waka_readme-blue?style=flat)](https://github.com/marketplace/actions/custom-waka-readme)

<picture>
	<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Twisuki/Twisuki/output/github-contribution-grid-snake-dark.svg" />
	<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Twisuki/Twisuki/output/github-contribution-grid-snake.svg">
	<img src="src/snake-light.svg" />
</picture>

## 联系方式 Contact me

- E-mail: [hi@twis.uk](mailto://hi@twis.uk)
- BiliBili: [Nya_Twisuki](https://space.bilibili.com/317707977)
- Twitter : [Su_Yang_233](https://x.com/suyang_233)

以及我会活跃的地方:

- Minecraft : [Nya_Twisuki](https://namemc.com/profile/Nya_Twisuki)
- Discord : Twisuki
- KOOK : Nya_Twisuki (#5313)
