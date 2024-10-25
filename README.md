  # **𝑴𝒂𝒕𝒆𝒖𝒔 𝑪𝒉𝒂𝒈𝒂𝒔**😼
- 𝐄𝐬𝐭𝐨𝐮 𝐢𝐧𝐭𝐞𝐫𝐞𝐬𝐬𝐚𝐝𝐨 𝐞𝐦 𝐚𝐩𝐫𝐞𝐧𝐝𝐞𝐫 𝐚 𝐩𝐫𝐨𝐠𝐫𝐚𝐦𝐚𝐫 𝐧𝐨𝐯𝐚𝐬 𝐥𝐢𝐧𝐠𝐮𝐚𝐠𝐞𝐧𝐬
- 𝐑𝐞𝐜𝐞𝐧𝐭𝐞 𝐞𝐬𝐭𝐨𝐮 𝐚𝐩𝐫𝐞𝐧𝐝𝐞𝐧𝐝𝐨 𝐚 𝐩𝐫𝐨𝐠𝐫𝐚𝐦𝐚𝐫 𝐚 𝐥𝐢𝐧𝐠𝐮𝐚𝐠𝐞𝐦 𝐝𝐞 𝐉𝐚𝐯𝐚𝐒𝐜𝐫𝐢𝐩𝐭 𝐞 𝐒𝐜𝐫𝐚𝐭𝐜𝐡

 ![](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
 ![](https://img.shields.io/badge/Scratch-4D97FF?style=for-the-badge&logo=Scratch&logoColor=white)       

 <div>
  <a href="https://github.com/Mateuuus">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Mateuuus&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="0m" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mateuuus&layout=compact&langs_count=7&theme=dark"/>
</div>
    
 #
 <div>
   <a href = "mailto:chagasmateus087@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
   <a href="https://instagram.com/matt.hc_" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 
  </div>
  name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps: 

      # Summary Cards
      - uses: actions/checkout@v2
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}

    
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Mateuuus
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
