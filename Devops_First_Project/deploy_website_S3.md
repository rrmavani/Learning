## Deploy to S3

### Modify docker compose
We can use already created images for aws cli.
Modify docker compose.

```docker
  aws:
    image: xueshanf/awscli
    volumes:
      - "$PWD:/app"
    working_dir: /app
    env_file: .env
```


### Run image
<details>
  <summary> 
    <code> docker-compose run --rm aws aws --version </code>
  </summary>

```bash
Pulling aws (xueshanf/awscli:)...
latest: Pulling from xueshanf/awscli
59bf1c3509f3: Pull complete
fcd201a8920c: Pull complete
f32692891df8: Pull complete
Digest: sha256:d10575022ceaed58139335f522667ee050e173524c4ad53a3adff35536902197
Status: Downloaded newer image for xueshanf/awscli:latest
Creating work_aws_run ... done
aws-cli/1.22.20 Python/3.9.7 Linux/5.10.104-linuxkit botocore/1.23.20
```

</details>

### Test authentication
<details>
  <summary> 
    <code> docker-compose run --rm aws aws s3 ls </code>
  </summary>
```bash
Creating work_aws_run ... done
2022-09-22 19:49:11 melearning.tk
```
</details>

### Deploy content
<details>
  <summary> 
    <code> docker-compose run --rm --entrypoint aws aws s3 cp --recursive website/ s3://melearning.tk </code>
  </summary>

```bash
Creating work_aws_run ... done
upload: website/.dockerignore to s3://melearning.tk/.dockerignore 
upload: website/_assets/.DS_Store to s3://melearning.tk/_assets/.DS_Store
upload: website/_css/images/ui-bg_flat_10_000000_40x100.png to s3://melearning.tk/_css/images/ui-bg_flat_10_000000_40x100.png
upload: website/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png to s3://melearning.tk/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png
upload: website/_css/images/ui-bg_glass_100_f0e7c7_1x400.png to s3://melearning.tk/_css/images/ui-bg_glass_100_f0e7c7_1x400.png
upload: website/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png to s3://melearning.tk/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png
upload: website/_css/fonts.css to s3://melearning.tk/_css/fonts.css  
upload: website/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png to s3://melearning.tk/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png
upload: website/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png to s3://melearning.tk/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png
upload: website/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png to s3://melearning.tk/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png
upload: website/_css/images/ui-icons_222222_256x240.png to s3://melearning.tk/_css/images/ui-icons_222222_256x240.png
upload: website/_css/images/ui-bg_glass_65_ffffff_1x400.png to s3://melearning.tk/_css/images/ui-bg_glass_65_ffffff_1x400.png
upload: website/_css/images/ui-icons_ffffff_256x240.png to s3://melearning.tk/_css/images/ui-icons_ffffff_256x240.png
upload: website/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png to s3://melearning.tk/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png
upload: website/_css/images/ui-icons_ffd27a_256x240.png to s3://melearning.tk/_css/images/ui-icons_ffd27a_256x240.png
upload: website/_css/jquery_widgets.css to s3://melearning.tk/_css/jquery_widgets.css
upload: website/_css/mobile.css to s3://melearning.tk/_css/mobile.css
upload: website/_css/images/ui-icons_cb7d20_256x240.png to s3://melearning.tk/_css/images/ui-icons_cb7d20_256x240.png
upload: website/_fonts/DejaVuSans-Bold-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.ttf
upload: website/_fonts/DejaVuSans-Bold-webfont.woff to s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.woff
upload: website/_fonts/DejaVuSans-Bold-webfont.svg to s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.svg
upload: website/_fonts/DejaVuSans-BoldOblique-webfont.eot to s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.eot
upload: website/_css/main.css to s3://melearning.tk/_css/main.css
upload: website/_css/images/ui-icons_228ef1_256x240.png to s3://melearning.tk/_css/images/ui-icons_228ef1_256x240.png
upload: website/_fonts/DejaVuSans-Bold-webfont.eot to s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.eot
upload: website/_fonts/DejaVuSans-BoldOblique-webfont.woff to s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.woff
upload: website/_fonts/DejaVuSans-Oblique-webfont.svg to s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.svg
upload: website/_fonts/DejaVuSans-BoldOblique-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.ttf
upload: website/_css/tablet.css to s3://melearning.tk/_css/tablet.css
upload: website/_css/images/ui-icons_ef8c08_256x240.png to s3://melearning.tk/_css/images/ui-icons_ef8c08_256x240.png
upload: website/_fonts/DejaVuSans-webfont.eot to s3://melearning.tk/_fonts/DejaVuSans-webfont.eot
upload: website/_fonts/DejaVuSans-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSans-webfont.ttf
upload: website/_fonts/DejaVuSans-webfont.svg to s3://melearning.tk/_fonts/DejaVuSans-webfont.svg
upload: website/_fonts/DejaVuSans-Oblique-webfont.eot to s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.eot
upload: website/_fonts/DejaVuSans-Oblique-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.ttf
upload: website/_fonts/DejaVuSansCondensed-Bold-webfont.svg to s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.svg
upload: website/_fonts/DejaVuSansCondensed-Bold-webfont.woff to s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.woff
upload: website/_fonts/DejaVuSansCondensed-Bold-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.ttf
upload: website/_fonts/DejaVuSans-webfont.woff to s3://melearning.tk/_fonts/DejaVuSans-webfont.woff
upload: website/_fonts/DejaVuSans-Oblique-webfont.woff to s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.woff
upload: website/_fonts/DejaVuSansCondensed-Oblique-webfont.eot to s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.eot
upload: website/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff to s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff
upload: website/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf
upload: website/_fonts/DejaVuSansCondensed-Bold-webfont.eot to s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.eot
upload: website/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg to s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg
upload: website/_fonts/DejaVuSansCondensed-webfont.svg to s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.svg
upload: website/_fonts/DejaVuSansCondensed-webfont.eot to s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.eot
upload: website/_fonts/DejaVuSansCondensed-Oblique-webfont.woff to s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.woff
upload: website/_fonts/DejaVuSansCondensed-Oblique-webfont.svg to s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.svg
upload: website/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf
upload: website/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot to s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot
upload: website/_fonts/DejaVuSans-BoldOblique-webfont.svg to s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.svg
upload: website/_fonts/DejaVuSansCondensed-webfont.woff to s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.woff
upload: website/_fonts/DejaVuSansCondensed-webfont.ttf to s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.ttf
upload: website/_fonts/DroidSerif-Bold-webfont.svg to s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.svg
upload: website/_fonts/DroidSerif-BoldItalic-webfont.ttf to s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.ttf
upload: website/_assets/backpack_main.psd to s3://melearning.tk/_assets/backpack_main.psd
upload: website/_fonts/DroidSerif-Bold-webfont.woff to s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.woff
upload: website/_fonts/DroidSerif-Italic-webfont.svg to s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.svg
upload: website/_fonts/DroidSerif-Bold-webfont.ttf to s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.ttf
upload: website/_fonts/DroidSerif-Italic-webfont.woff to s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.woff
upload: website/_fonts/DroidSerif-BoldItalic-webfont.woff to s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.woff
upload: website/_fonts/DroidSerif-Italic-webfont.ttf to s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.ttf
upload: website/_fonts/DroidSerif-BoldItalic-webfont.svg to s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.svg
upload: website/_fonts/DroidSerif-BoldItalic-webfont.eot to s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.eot
upload: website/_fonts/DroidSerif-Regular-webfont.ttf to s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.ttf
upload: website/_fonts/DroidSerif-Regular-webfont.woff to s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.woff
upload: website/_fonts/DroidSerif-Italic-webfont.eot to s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.eot
upload: website/_fonts/font_licenses/DejaVu Fonts License.txt to s3://melearning.tk/_fonts/font_licenses/DejaVu Fonts License.txt
upload: website/_fonts/DroidSerif-Bold-webfont.eot to s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.eot
upload: website/_images/asterisk.gif to s3://melearning.tk/_images/asterisk.gif
upload: website/_fonts/font_licenses/Google Android License.txt to s3://melearning.tk/_fonts/font_licenses/Google Android License.txt
upload: website/_images/backpack_bug.gif to s3://melearning.tk/_images/backpack_bug.gif
upload: website/_images/back_bug.gif to s3://melearning.tk/_images/back_bug.gif
upload: website/_fonts/DroidSerif-Regular-webfont.svg to s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.svg
upload: website/_fonts/DroidSerif-Regular-webfont.eot to s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.eot
upload: website/_images/book_bug.gif to s3://melearning.tk/_images/book_bug.gif
upload: website/_images/calm_bug.gif to s3://melearning.tk/_images/calm_bug.gif
upload: website/_images/calm_desc_bug.gif to s3://melearning.tk/_images/calm_desc_bug.gif
upload: website/_images/big_sur.jpg to s3://melearning.tk/_images/big_sur.jpg
upload: website/_images/bikes.jpg to s3://melearning.tk/_images/bikes.jpg
upload: website/_images/cycle_desc_bug.gif to s3://melearning.tk/_images/cycle_desc_bug.gif
upload: website/_images/breakup.jpg to s3://melearning.tk/_images/breakup.jpg
upload: website/_images/cycle_logo.png to s3://melearning.tk/_images/cycle_logo.png
upload: website/_assets/1280_models.tif to s3://melearning.tk/_assets/1280_models.tif
upload: website/_images/desert_desc_bug.gif to s3://melearning.tk/_images/desert_desc_bug.gif
upload: website/_images/desert_bug.gif to s3://melearning.tk/_images/desert_bug.gif
upload: website/_images/bridge.jpg to s3://melearning.tk/_images/bridge.jpg
upload: website/_images/emerald_bay.jpg to s3://melearning.tk/_images/emerald_bay.jpg
upload: website/_images/backpack_main.jpg to s3://melearning.tk/_images/backpack_main.jpg
upload: website/_images/cyclist.jpg to s3://melearning.tk/_images/cyclist.jpg
upload: website/_images/kids_desc_bug.gif to s3://melearning.tk/_images/kids_desc_bug.gif
upload: website/_images/logo.gif to s3://melearning.tk/_images/logo.gif
upload: website/_images/map_bigsur.gif to s3://melearning.tk/_images/map_bigsur.gif
upload: website/_images/map_channel.gif to s3://melearning.tk/_images/map_channel.gif
upload: website/_images/map_valley.gif to s3://melearning.tk/_images/map_valley.gif
upload: website/_images/map_whitney.gif to s3://melearning.tk/_images/map_whitney.gif
upload: website/_images/more_bug.gif to s3://melearning.tk/_images/more_bug.gif
upload: website/_images/map_yosemite.gif to s3://melearning.tk/_images/map_yosemite.gif
upload: website/_images/flag.jpg to s3://melearning.tk/_images/flag.jpg
upload: website/_images/nature_desc_bug.gif to s3://melearning.tk/_images/nature_desc_bug.gif
upload: website/_images/looking.jpg to s3://melearning.tk/_images/looking.jpg
upload: website/_images/mission_look.jpg to s3://melearning.tk/_images/mission_look.jpg
upload: website/_images/return_top.gif to s3://melearning.tk/_images/return_top.gif
upload: website/_images/snow_desc_bug.gif to s3://melearning.tk/_images/snow_desc_bug.gif
upload: website/_images/oranges.jpg to s3://melearning.tk/_images/oranges.jpg
upload: website/_images/star_bullet.gif to s3://melearning.tk/_images/star_bullet.gif
upload: website/_images/taste_bug.gif to s3://melearning.tk/_images/taste_bug.gif
upload: website/_images/springs_desc_bug.gif to s3://melearning.tk/_images/springs_desc_bug.gif
upload: website/_images/taste_desc_bug.gif to s3://melearning.tk/_images/taste_desc_bug.gif
upload: website/_images/thead_back.gif to s3://melearning.tk/_images/thead_back.gif
upload: website/_images/tour_badge.png to s3://melearning.tk/_images/tour_badge.png
upload: website/_scripts/jquery-1.5.1.min.js to s3://melearning.tk/_scripts/jquery-1.5.1.min.js
upload: website/_scripts/menus.js to s3://melearning.tk/_scripts/menus.js
upload: website/config.yml to s3://melearning.tk/config.yml        
upload: website/explorers.htm to s3://melearning.tk/explorers.htm  
upload: website/_scripts/jquery-ui-1.8.10.custom.min.js to s3://melearning.tk/_scripts/jquery-ui-1.8.10.custom.min.js
upload: website/index.htm to s3://melearning.tk/index.htm          
upload: website/_images/wrapper_back.jpg to s3://melearning.tk/_images/wrapper_back.jpg
upload: website/contact.htm to s3://melearning.tk/contact.htm      
upload: website/mission.htm to s3://melearning.tk/mission.htm      
upload: website/resources.htm to s3://melearning.tk/resources.htm  
upload: website/resources/faq.htm to s3://melearning.tk/resources/faq.htm
upload: website/_images/home_page_back.jpg to s3://melearning.tk/_images/home_page_back.jpg
upload: website/static/_assets/.DS_Store to s3://melearning.tk/static/_assets/.DS_Store
upload: website/static/_css/fonts.css to s3://melearning.tk/static/_css/fonts.css
upload: website/static/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png to s3://melearning.tk/static/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png
upload: website/static/_css/images/ui-bg_flat_10_000000_40x100.png to s3://melearning.tk/static/_css/images/ui-bg_flat_10_000000_40x100.png
upload: website/static/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png to s3://melearning.tk/static/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png
upload: website/static/_css/images/ui-bg_glass_100_f0e7c7_1x400.png to s3://melearning.tk/static/_css/images/ui-bg_glass_100_f0e7c7_1x400.png
upload: website/static/_css/images/ui-bg_glass_65_ffffff_1x400.png to s3://melearning.tk/static/_css/images/ui-bg_glass_65_ffffff_1x400.png
upload: website/static/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png to s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png
upload: website/static/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png to s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png
upload: website/static/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png to s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png
upload: website/static/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png to s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png
upload: website/static/_css/images/ui-icons_222222_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_222222_256x240.png
upload: website/static/_css/images/ui-icons_228ef1_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_228ef1_256x240.png
upload: website/static/_css/images/ui-icons_cb7d20_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_cb7d20_256x240.png
upload: website/static/_css/images/ui-icons_ef8c08_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_ef8c08_256x240.png
upload: website/static/_css/images/ui-icons_ffd27a_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_ffd27a_256x240.png
upload: website/static/_css/images/ui-icons_ffffff_256x240.png to s3://melearning.tk/static/_css/images/ui-icons_ffffff_256x240.png
upload: website/static/_css/main.css to s3://melearning.tk/static/_css/main.css
upload: website/static/_css/jquery_widgets.css to s3://melearning.tk/static/_css/jquery_widgets.css
upload: website/static/_css/mobile.css to s3://melearning.tk/static/_css/mobile.css
upload: website/static/_css/tablet.css to s3://melearning.tk/static/_css/tablet.css
upload: website/static/_fonts/DejaVuSans-Bold-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.eot
upload: website/static/_fonts/DejaVuSans-Bold-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.svg
upload: website/static/_fonts/DejaVuSans-BoldOblique-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.woff
upload: website/static/_fonts/DejaVuSans-Bold-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.woff
upload: website/static/_fonts/DejaVuSans-Oblique-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.woff
upload: website/static/_fonts/DejaVuSans-BoldOblique-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.eot
upload: website/static/_fonts/DejaVuSans-Oblique-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.ttf
upload: website/static/_fonts/DejaVuSans-BoldOblique-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.ttf
upload: website/static/_fonts/DejaVuSans-Oblique-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.eot
upload: website/static/_fonts/DejaVuSans-Oblique-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.svg
upload: website/static/_fonts/DejaVuSans-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSans-webfont.eot
upload: website/static/_fonts/DejaVuSans-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSans-webfont.ttf
upload: website/static/_fonts/DejaVuSans-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSans-webfont.woff
upload: website/static/_fonts/DejaVuSansCondensed-Bold-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.eot
upload: website/static/_fonts/DejaVuSansCondensed-Bold-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.svg
upload: website/static/_fonts/DejaVuSans-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSans-webfont.svg
upload: website/static/_fonts/DejaVuSansCondensed-Bold-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.woff
upload: website/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg
upload: website/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot
upload: website/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf
upload: website/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff
upload: website/static/_fonts/DejaVuSansCondensed-Oblique-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.eot
upload: website/static/_fonts/DejaVuSansCondensed-Oblique-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.svg
upload: website/static/_fonts/DejaVuSansCondensed-Oblique-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.woff
upload: website/static/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf
upload: website/static/_fonts/DejaVuSansCondensed-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.svg
upload: website/static/_fonts/DroidSerif-Bold-webfont.eot to s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.eot
upload: website/static/_fonts/DejaVuSansCondensed-webfont.woff to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.woff
upload: website/static/_fonts/DejaVuSansCondensed-webfont.eot to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.eot
upload: website/static/_fonts/DejaVuSansCondensed-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.ttf
upload: website/static/_fonts/DroidSerif-Bold-webfont.ttf to s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.ttf
upload: website/static/_fonts/DroidSerif-BoldItalic-webfont.eot to s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.eot
upload: website/static/_fonts/DroidSerif-BoldItalic-webfont.svg to s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.svg
upload: website/static/_fonts/DroidSerif-Bold-webfont.svg to s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.svg
upload: website/static/_fonts/DroidSerif-Bold-webfont.woff to s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.woff
upload: website/static/_fonts/DroidSerif-BoldItalic-webfont.woff to s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.woff
upload: website/static/_fonts/DroidSerif-Italic-webfont.svg to s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.svg
upload: website/static/_fonts/DroidSerif-Italic-webfont.eot to s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.eot
upload: website/static/_fonts/DroidSerif-Italic-webfont.ttf to s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.ttf
upload: website/static/_fonts/DroidSerif-Italic-webfont.woff to s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.woff
upload: website/static/_fonts/DroidSerif-BoldItalic-webfont.ttf to s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.ttf
upload: website/static/_fonts/DroidSerif-Regular-webfont.eot to s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.eot
upload: website/static/_fonts/DroidSerif-Regular-webfont.ttf to s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.ttf
upload: website/static/_fonts/DejaVuSans-Bold-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.ttf
upload: website/static/_fonts/DroidSerif-Regular-webfont.woff to s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.woff
upload: website/static/_fonts/font_licenses/DejaVu Fonts License.txt to s3://melearning.tk/static/_fonts/font_licenses/DejaVu Fonts License.txt
upload: website/static/_fonts/DroidSerif-Regular-webfont.svg to s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.svg
upload: website/static/_fonts/font_licenses/Google Android License.txt to s3://melearning.tk/static/_fonts/font_licenses/Google Android License.txt
upload: website/static/_fonts/DejaVuSansCondensed-Bold-webfont.ttf to s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.ttf
upload: website/static/_images/asterisk.gif to s3://melearning.tk/static/_images/asterisk.gif
upload: website/static/_images/back_bug.gif to s3://melearning.tk/static/_images/back_bug.gif
upload: website/static/_fonts/DejaVuSans-BoldOblique-webfont.svg to s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.svg
upload: website/static/_images/book_bug.gif to s3://melearning.tk/static/_images/book_bug.gif
upload: website/static/_images/bridge.jpg to s3://melearning.tk/static/_images/bridge.jpg
upload: website/static/_images/breakup.jpg to s3://melearning.tk/static/_images/breakup.jpg
upload: website/static/_images/calm_bug.gif to s3://melearning.tk/static/_images/calm_bug.gif
upload: website/static/_images/calm_desc_bug.gif to s3://melearning.tk/static/_images/calm_desc_bug.gif
upload: website/static/_images/backpack_main.jpg to s3://melearning.tk/static/_images/backpack_main.jpg
upload: website/static/_images/cycle_desc_bug.gif to s3://melearning.tk/static/_images/cycle_desc_bug.gif
upload: website/static/_images/cycle_logo.png to s3://melearning.tk/static/_images/cycle_logo.png
upload: website/static/_images/bikes.jpg to s3://melearning.tk/static/_images/bikes.jpg
upload: website/static/_images/desert_bug.gif to s3://melearning.tk/static/_images/desert_bug.gif
upload: website/static/_images/desert_desc_bug.gif to s3://melearning.tk/static/_images/desert_desc_bug.gif
upload: website/static/_images/cyclist.jpg to s3://melearning.tk/static/_images/cyclist.jpg
upload: website/static/_images/flag.jpg to s3://melearning.tk/static/_images/flag.jpg
upload: website/static/_assets/1280_models.tif to s3://melearning.tk/static/_assets/1280_models.tif
upload: website/static/_images/kids_desc_bug.gif to s3://melearning.tk/static/_images/kids_desc_bug.gif
upload: website/static/_images/logo.gif to s3://melearning.tk/static/_images/logo.gif
upload: website/static/_images/emerald_bay.jpg to s3://melearning.tk/static/_images/emerald_bay.jpg
upload: website/static/_images/big_sur.jpg to s3://melearning.tk/static/_images/big_sur.jpg
upload: website/static/_images/map_bigsur.gif to s3://melearning.tk/static/_images/map_bigsur.gif
upload: website/static/_images/map_whitney.gif to s3://melearning.tk/static/_images/map_whitney.gif
upload: website/static/_images/map_channel.gif to s3://melearning.tk/static/_images/map_channel.gif
upload: website/static/_images/map_yosemite.gif to s3://melearning.tk/static/_images/map_yosemite.gif
upload: website/static/_images/map_valley.gif to s3://melearning.tk/static/_images/map_valley.gif
upload: website/static/_images/looking.jpg to s3://melearning.tk/static/_images/looking.jpg
upload: website/static/_images/more_bug.gif to s3://melearning.tk/static/_images/more_bug.gif
upload: website/static/_images/mission_look.jpg to s3://melearning.tk/static/_images/mission_look.jpg
upload: website/static/_images/nature_desc_bug.gif to s3://melearning.tk/static/_images/nature_desc_bug.gif
upload: website/static/_images/home_page_back.jpg to s3://melearning.tk/static/_images/home_page_back.jpg
upload: website/static/_images/backpack_bug.gif to s3://melearning.tk/static/_images/backpack_bug.gif
upload: website/static/_images/snow_desc_bug.gif to s3://melearning.tk/static/_images/snow_desc_bug.gif
upload: website/static/_images/return_top.gif to s3://melearning.tk/static/_images/return_top.gif
upload: website/static/_images/springs_desc_bug.gif to s3://melearning.tk/static/_images/springs_desc_bug.gif
upload: website/static/_images/taste_bug.gif to s3://melearning.tk/static/_images/taste_bug.gif
upload: website/static/_images/star_bullet.gif to s3://melearning.tk/static/_images/star_bullet.gif
upload: website/static/_images/taste_desc_bug.gif to s3://melearning.tk/static/_images/taste_desc_bug.gif
upload: website/static/_images/thead_back.gif to s3://melearning.tk/static/_images/thead_back.gif
upload: website/static/_images/tour_badge.png to s3://melearning.tk/static/_images/tour_badge.png
upload: website/static/_images/oranges.jpg to s3://melearning.tk/static/_images/oranges.jpg
upload: website/static/_scripts/jquery-1.5.1.min.js to s3://melearning.tk/static/_scripts/jquery-1.5.1.min.js
upload: website/static/_images/wrapper_back.jpg to s3://melearning.tk/static/_images/wrapper_back.jpg
upload: website/static/_scripts/menus.js to s3://melearning.tk/static/_scripts/menus.js
upload: website/static/tours/tour_detail_backpack.htm to s3://melearning.tk/static/tours/tour_detail_backpack.htm
upload: website/static/tours/tour_detail_bigsur.htm to s3://melearning.tk/static/tours/tour_detail_bigsur.htm
upload: website/support.htm to s3://melearning.tk/support.htm     
upload: website/static/resources/faq.htm to s3://melearning.tk/static/resources/faq.htm
upload: website/static/_assets/backpack_main.psd to s3://melearning.tk/static/_assets/backpack_main.psd
upload: website/tours/tour_detail_bigsur.htm to s3://melearning.tk/tours/tour_detail_bigsur.htm
upload: website/tours.htm to s3://melearning.tk/tours.htm         
upload: website/tours/tour_detail_backpack.htm to s3://melearning.tk/tours/tour_detail_backpack.htm
upload: website/template.htm to s3://melearning.tk/template.htm   
upload: website/widgets.htm to s3://melearning.tk/widgets.htm     
upload: website/static/_scripts/jquery-ui-1.8.10.custom.min.js to s3://melearning.tk/static/_scripts/jquery-ui-1.8.10.custom.min.js
```
</details>

### Visit website
- Know website URL by below command
```bash
$ docker-compose run --rm terraform output
Creating work_terraform_run ... done
website_bucket_url = "melearning.tk.s3-website-us-east-1.amazonaws.com"
```

- Open browser and visite the website
![website](assets/from_s3.png)