![unnamed](https://github.com/user-attachments/assets/43571b1b-baa9-4e7b-a0fb-73add4c7062a)
# Hola! soy Paulo!!

Soy un desarrollador apasionado por crear software que simplifique la vida de las personas. Actualmente, estoy enfocado en el desarrollo de soluciones tecnológicas para el sector comercial, uniendo la lógica de programación con las necesidades reales del mercado.

Soy estudiante de Ingeniería en Sistemas de la Información en la Facultad Regional Córdoba de la Universidad Tecnológica Nacional. 

Mis contactos: 
- Github: https://github.com/PauloTorres12
- Gmail: torrespaulo33@gmail.com

# Estadisticas de Github
[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com?user=PauloTorres12&theme=highcontrast&locale=es)](https://git.io/streak-stats)

.github/workflows/metrics.yml

name: Metrics

on:
  schedule:
    - cron: "0 6 * * *" # 3 AM Argentina (UTC-3 → 6 AM UTC)
  workflow_dispatch:

jobs:
  github-metrics:
    runs-on: ubuntu-latest

    steps:
      - name: Generate metrics
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}

          user: TU_USUARIO_GITHUB
          template: classic

          base: header, activity, community, repositories

          plugin_languages: yes
          plugin_languages_limit: 8
          plugin_languages_sections: most-used


