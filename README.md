### Hi :)
- any pronous
  <div>
    <a href="https://pokemondb.net/pokedex/oshawott"><img src="https://img.pokemondb.net/sprites/black-white-2/anim/shiny/oshawott.gif" alt="Oshawott"></a>
  </div>
  <hr>
  <div>
    <a href="https://github.com/HakuAkai">
    <img width="400" src="https://github-readme-stats.vercel.app/api?username=hakuakai&show_icons=true&theme=midnight-purple&include_all_commits=true&count_private=true"/><br>
    <img width="400" src="https://github-readme-stats.vercel.app/api/top-langs/?username=hakuakai&layout=compact&langs_count=7&theme=midnight-purple"/>
  </div>
  <div style="display: inline_block"><br>
    <img align="center" alt="HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  </div>
  <hr>
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
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: HakuAkai
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
