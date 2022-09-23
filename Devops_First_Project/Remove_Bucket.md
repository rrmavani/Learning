# Remove Bucket

## Empty bucket
Remove all the content of bucket

<details>
<summary><code>docker-compose run --rm --entrypoint aws aws s3 rm s3://melearning.tk --recursive</code>
</summary>

```bash
Creating work_aws_run ... done
delete: s3://melearning.tk/.dockerignore
delete: s3://melearning.tk/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png
delete: s3://melearning.tk/_assets/backpack_main.psd
delete: s3://melearning.tk/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png
delete: s3://melearning.tk/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png
delete: s3://melearning.tk/_css/fonts.css
delete: s3://melearning.tk/_assets/1280_models.tif
delete: s3://melearning.tk/_css/images/ui-bg_glass_65_ffffff_1x400.png
delete: s3://melearning.tk/_assets/.DS_Store
delete: s3://melearning.tk/_css/images/ui-icons_222222_256x240.png
delete: s3://melearning.tk/_css/images/ui-bg_flat_10_000000_40x100.png
delete: s3://melearning.tk/_css/images/ui-icons_cb7d20_256x240.png
delete: s3://melearning.tk/_css/images/ui-icons_ef8c08_256x240.png
delete: s3://melearning.tk/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png
delete: s3://melearning.tk/_css/main.css
delete: s3://melearning.tk/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png
delete: s3://melearning.tk/_css/jquery_widgets.css
delete: s3://melearning.tk/_css/tablet.css
delete: s3://melearning.tk/_css/images/ui-icons_ffffff_256x240.png
delete: s3://melearning.tk/_css/images/ui-icons_ffd27a_256x240.png
delete: s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSans-Bold-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.svg
delete: s3://melearning.tk/_css/images/ui-icons_228ef1_256x240.png
delete: s3://melearning.tk/_css/images/ui-bg_glass_100_f0e7c7_1x400.png
delete: s3://melearning.tk/_css/mobile.css
delete: s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSans-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSans-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSans-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSans-BoldOblique-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSans-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.eot
delete: s3://melearning.tk/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png
delete: s3://melearning.tk/_fonts/DejaVuSans-Oblique-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Bold-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-Oblique-webfont.woff
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.svg
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.eot
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.ttf
delete: s3://melearning.tk/_fonts/DejaVuSansCondensed-webfont.woff
delete: s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.eot
delete: s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.svg
delete: s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.woff
delete: s3://melearning.tk/_fonts/DroidSerif-Bold-webfont.ttf
delete: s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.eot
delete: s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.svg
delete: s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.ttf
delete: s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.eot
delete: s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.svg
delete: s3://melearning.tk/_fonts/DroidSerif-BoldItalic-webfont.woff
delete: s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.ttf
delete: s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.svg
delete: s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.eot
delete: s3://melearning.tk/_fonts/DroidSerif-Italic-webfont.woff
delete: s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.ttf
delete: s3://melearning.tk/_fonts/DroidSerif-Regular-webfont.woff
delete: s3://melearning.tk/_fonts/font_licenses/Google Android License.txt
delete: s3://melearning.tk/_images/asterisk.gif
delete: s3://melearning.tk/_images/back_bug.gif
delete: s3://melearning.tk/_images/backpack_bug.gif
delete: s3://melearning.tk/_fonts/font_licenses/DejaVu Fonts License.txt
delete: s3://melearning.tk/_images/big_sur.jpg
delete: s3://melearning.tk/_images/backpack_main.jpg
delete: s3://melearning.tk/_images/bikes.jpg
delete: s3://melearning.tk/_images/book_bug.gif
delete: s3://melearning.tk/_images/breakup.jpg
delete: s3://melearning.tk/_images/calm_desc_bug.gif
delete: s3://melearning.tk/_images/bridge.jpg
delete: s3://melearning.tk/_images/calm_bug.gif
delete: s3://melearning.tk/_images/cycle_logo.png
delete: s3://melearning.tk/_images/cycle_desc_bug.gif
delete: s3://melearning.tk/_images/cyclist.jpg
delete: s3://melearning.tk/_images/desert_desc_bug.gif
delete: s3://melearning.tk/_images/desert_bug.gif
delete: s3://melearning.tk/_images/emerald_bay.jpg
delete: s3://melearning.tk/_images/kids_desc_bug.gif
delete: s3://melearning.tk/_images/map_bigsur.gif
delete: s3://melearning.tk/_images/logo.gif
delete: s3://melearning.tk/_images/looking.jpg
delete: s3://melearning.tk/_images/home_page_back.jpg
delete: s3://melearning.tk/_images/flag.jpg
delete: s3://melearning.tk/_images/map_whitney.gif
delete: s3://melearning.tk/_images/map_yosemite.gif
delete: s3://melearning.tk/_images/map_channel.gif
delete: s3://melearning.tk/_images/map_valley.gif
delete: s3://melearning.tk/_images/mission_look.jpg
delete: s3://melearning.tk/_images/snow_desc_bug.gif
delete: s3://melearning.tk/_images/nature_desc_bug.gif
delete: s3://melearning.tk/_images/oranges.jpg
delete: s3://melearning.tk/_images/return_top.gif
delete: s3://melearning.tk/_images/taste_desc_bug.gif
delete: s3://melearning.tk/_images/taste_bug.gif
delete: s3://melearning.tk/_images/more_bug.gif
delete: s3://melearning.tk/_images/tour_badge.png
delete: s3://melearning.tk/_images/thead_back.gif
delete: s3://melearning.tk/_images/springs_desc_bug.gif
delete: s3://melearning.tk/_scripts/menus.js
delete: s3://melearning.tk/config.yml
delete: s3://melearning.tk/contact.htm
delete: s3://melearning.tk/explorers.htm
delete: s3://melearning.tk/index.htm
delete: s3://melearning.tk/mission.htm
delete: s3://melearning.tk/resources.htm
delete: s3://melearning.tk/static/_assets/.DS_Store
delete: s3://melearning.tk/resources/faq.htm
delete: s3://melearning.tk/static/_assets/1280_models.tif
delete: s3://melearning.tk/static/_assets/backpack_main.psd
delete: s3://melearning.tk/static/_css/fonts.css
delete: s3://melearning.tk/static/_css/images/ui-bg_diagonals-thick_18_b81900_40x40.png
delete: s3://melearning.tk/static/_css/images/ui-bg_flat_10_000000_40x100.png
delete: s3://melearning.tk/static/_css/images/ui-bg_glass_65_ffffff_1x400.png
delete: s3://melearning.tk/static/_css/images/ui-bg_diagonals-thick_20_666666_40x40.png
delete: s3://melearning.tk/_images/star_bullet.gif
delete: s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_100_f6f6f6_1x100.png
delete: s3://melearning.tk/static/_css/images/ui-bg_glass_100_f0e7c7_1x400.png
delete: s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_35_cb7d20_1x100.png
delete: s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_100_eeeeee_1x100.png
delete: s3://melearning.tk/_images/wrapper_back.jpg
delete: s3://melearning.tk/static/_css/images/ui-icons_222222_256x240.png
delete: s3://melearning.tk/static/_css/images/ui-icons_cb7d20_256x240.png
delete: s3://melearning.tk/static/_css/images/ui-icons_ef8c08_256x240.png
delete: s3://melearning.tk/static/_css/images/ui-bg_highlight-soft_75_ffe45c_1x100.png
delete: s3://melearning.tk/static/_css/images/ui-icons_228ef1_256x240.png
delete: s3://melearning.tk/_scripts/jquery-ui-1.8.10.custom.min.js
delete: s3://melearning.tk/static/_css/images/ui-icons_ffd27a_256x240.png
delete: s3://melearning.tk/_scripts/jquery-1.5.1.min.js
delete: s3://melearning.tk/static/_css/images/ui-icons_ffffff_256x240.png
delete: s3://melearning.tk/static/_css/jquery_widgets.css
delete: s3://melearning.tk/static/_css/main.css
delete: s3://melearning.tk/static/_css/mobile.css
delete: s3://melearning.tk/static/_css/tablet.css
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Bold-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSans-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSans-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSans-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSans-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Bold-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-BoldOblique-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.svg
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSans-Oblique-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSans-BoldOblique-webfont.woff
delete: s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.svg
delete: s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.eot
delete: s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DroidSerif-Bold-webfont.woff
delete: s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.eot
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.woff
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-Oblique-webfont.woff
delete: s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.eot
delete: s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.svg
delete: s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.eot
delete: s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.woff
delete: s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.ttf
delete: s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.woff
delete: s3://melearning.tk/static/_fonts/DroidSerif-Regular-webfont.svg
delete: s3://melearning.tk/static/_images/asterisk.gif
delete: s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.svg
delete: s3://melearning.tk/static/_fonts/font_licenses/Google Android License.txt
delete: s3://melearning.tk/static/_fonts/DroidSerif-BoldItalic-webfont.ttf
delete: s3://melearning.tk/static/_images/backpack_bug.gif
delete: s3://melearning.tk/static/_images/backpack_main.jpg
delete: s3://melearning.tk/static/_fonts/DroidSerif-Italic-webfont.woff
delete: s3://melearning.tk/static/_images/bikes.jpg
delete: s3://melearning.tk/static/_images/breakup.jpg
delete: s3://melearning.tk/static/_images/book_bug.gif
delete: s3://melearning.tk/static/_images/bridge.jpg
delete: s3://melearning.tk/static/_images/cycle_desc_bug.gif
delete: s3://melearning.tk/static/_images/back_bug.gif
delete: s3://melearning.tk/static/_images/calm_bug.gif
delete: s3://melearning.tk/static/_fonts/font_licenses/DejaVu Fonts License.txt
delete: s3://melearning.tk/static/_images/big_sur.jpg
delete: s3://melearning.tk/static/_images/calm_desc_bug.gif
delete: s3://melearning.tk/static/_fonts/DejaVuSansCondensed-webfont.svg
delete: s3://melearning.tk/static/_images/cycle_logo.png
delete: s3://melearning.tk/static/_images/home_page_back.jpg
delete: s3://melearning.tk/static/_images/cyclist.jpg
delete: s3://melearning.tk/static/_images/logo.gif
delete: s3://melearning.tk/static/_images/flag.jpg
delete: s3://melearning.tk/static/_images/desert_desc_bug.gif
delete: s3://melearning.tk/static/_images/desert_bug.gif
delete: s3://melearning.tk/static/_images/kids_desc_bug.gif
delete: s3://melearning.tk/static/_images/emerald_bay.jpg
delete: s3://melearning.tk/static/_images/looking.jpg
delete: s3://melearning.tk/static/_images/map_bigsur.gif
delete: s3://melearning.tk/static/_images/map_channel.gif
delete: s3://melearning.tk/static/_images/more_bug.gif
delete: s3://melearning.tk/static/_images/return_top.gif
delete: s3://melearning.tk/static/_images/map_valley.gif
delete: s3://melearning.tk/static/_images/snow_desc_bug.gif
delete: s3://melearning.tk/static/_images/springs_desc_bug.gif
delete: s3://melearning.tk/static/_images/nature_desc_bug.gif
delete: s3://melearning.tk/static/_images/taste_bug.gif
delete: s3://melearning.tk/static/_images/star_bullet.gif
delete: s3://melearning.tk/static/_images/taste_desc_bug.gif
delete: s3://melearning.tk/static/_images/thead_back.gif
delete: s3://melearning.tk/static/_images/tour_badge.png
delete: s3://melearning.tk/static/_images/mission_look.jpg
delete: s3://melearning.tk/static/_scripts/jquery-1.5.1.min.js
delete: s3://melearning.tk/static/_images/map_yosemite.gif
delete: s3://melearning.tk/static/_scripts/jquery-ui-1.8.10.custom.min.js
delete: s3://melearning.tk/static/_images/wrapper_back.jpg
delete: s3://melearning.tk/static/tours/tour_detail_backpack.htm
delete: s3://melearning.tk/static/tours/tour_detail_bigsur.htm
delete: s3://melearning.tk/template.htm
delete: s3://melearning.tk/support.htm
delete: s3://melearning.tk/tours.htm
delete: s3://melearning.tk/tours/tour_detail_backpack.htm
delete: s3://melearning.tk/static/_scripts/menus.js
delete: s3://melearning.tk/tours/tour_detail_bigsur.htm
delete: s3://melearning.tk/static/resources/faq.htm
delete: s3://melearning.tk/static/_images/map_whitney.gif
delete: s3://melearning.tk/static/_images/oranges.jpg
delete: s3://melearning.tk/widgets.htm
```

</details>

## Delete all the resources
Run terraform destroy to delete all the resources created for s3 bucket

<details>
<summary>
<code>docker-compose run --rm terraform destroy</code></Summary>

```bash
Creating work_terraform_run ... done
data.aws_iam_policy_document.bucket_policy: Reading...
aws_s3_bucket.website: Refreshing state... [id=melearning.tk]
data.aws_iam_policy_document.bucket_policy: Read complete after 0s [id=715928839]
aws_s3_bucket_policy.website: Refreshing state... [id=melearning.tk]
aws_s3_bucket_website_configuration.website: Refreshing state... [id=melearning.tk]
aws_s3_bucket_acl.website: Refreshing state... [id=melearning.tk,public-read]

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
  - destroy

Terraform will perform the following actions:

  # aws_s3_bucket.website will be destroyed
  - resource "aws_s3_bucket" "website" {
      - arn                         = "arn:aws:s3:::melearning.tk" -> null
      - bucket                      = "melearning.tk" -> null
      - bucket_domain_name          = "melearning.tk.s3.amazonaws.com" -> null
      - bucket_regional_domain_name = "melearning.tk.s3.amazonaws.com" -> null
      - force_destroy               = false -> null
      - hosted_zone_id              = "Z3AQBSTGFYJSTF" -> null
      - id                          = "melearning.tk" -> null
      - object_lock_enabled         = false -> null
      - policy                      = jsonencode(
            {
              - Statement = [
                  - {
                      - Action    = "s3:GetObject"
                      - Effect    = "Allow"
                      - Principal = "*"
                      - Resource  = "arn:aws:s3:::melearning.tk/*"
                      - Sid       = "PublicReadGetObject"
                    },
                ]
              - Version   = "2012-10-17"
            }
        ) -> null
      - region                      = "us-east-1" -> null
      - request_payer               = "BucketOwner" -> null
      - tags                        = {} -> null
      - tags_all                    = {
          - "use"                  = "useast1_FirstProject"
          - "useast1_FirstProject" = "use"
        } -> null
      - website_domain              = "s3-website-us-east-1.amazonaws.com" -> null
      - website_endpoint            = "melearning.tk.s3-website-us-east-1.amazonaws.com" -> null

      - grant {
          - permissions = [
              - "READ",
            ] -> null
          - type        = "Group" -> null
          - uri         = "http://acs.amazonaws.com/groups/global/AllUsers" -> null
        }
      - grant {
          - id          = "8384cfcd6a0d40ed63cc1e3f8d2355118267ccd83b3e956fddf9d6877ed09646" -> null
          - permissions = [
              - "FULL_CONTROL",
            ] -> null
          - type        = "CanonicalUser" -> null
        }

      - versioning {
          - enabled    = false -> null
          - mfa_delete = false -> null
        }

      - website {
          - error_document = "error.html" -> null
          - index_document = "index.htm" -> null
        }
    }

  # aws_s3_bucket_acl.website will be destroyed
  - resource "aws_s3_bucket_acl" "website" {
      - acl    = "public-read" -> null
      - bucket = "melearning.tk" -> null
      - id     = "melearning.tk,public-read" -> null

      - access_control_policy {
          - grant {
              - permission = "READ" -> null

              - grantee {
                  - type = "Group" -> null
                  - uri  = "http://acs.amazonaws.com/groups/global/AllUsers" -> null
                }
            }
          - grant {
              - permission = "FULL_CONTROL" -> null

              - grantee {
                  - display_name = "kindredcloud" -> null
                  - id           = "8384cfcd6a0d40ed63cc1e3f8d2355118267ccd83b3e956fddf9d6877ed09646" -> null
                  - type         = "CanonicalUser" -> null
                }
            }

          - owner {
              - display_name = "kindredcloud" -> null
              - id           = "8384cfcd6a0d40ed63cc1e3f8d2355118267ccd83b3e956fddf9d6877ed09646" -> null
            }
        }
    }

  # aws_s3_bucket_policy.website will be destroyed
  - resource "aws_s3_bucket_policy" "website" {
      - bucket = "melearning.tk" -> null
      - id     = "melearning.tk" -> null
      - policy = jsonencode(
            {
              - Statement = [
                  - {
                      - Action    = "s3:GetObject"
                      - Effect    = "Allow"
                      - Principal = "*"
                      - Resource  = "arn:aws:s3:::melearning.tk/*"
                      - Sid       = "PublicReadGetObject"
                    },
                ]
              - Version   = "2012-10-17"
            }
        ) -> null
    }

  # aws_s3_bucket_website_configuration.website will be destroyed
  - resource "aws_s3_bucket_website_configuration" "website" {
      - bucket           = "melearning.tk" -> null
      - id               = "melearning.tk" -> null
      - website_domain   = "s3-website-us-east-1.amazonaws.com" -> null
      - website_endpoint = "melearning.tk.s3-website-us-east-1.amazonaws.com" -> null

      - error_document {
          - key = "error.html" -> null
        }

      - index_document {
          - suffix = "index.htm" -> null
        }
    }

Plan: 0 to add, 0 to change, 4 to destroy.

Changes to Outputs:
  - website_bucket_url = "melearning.tk.s3-website-us-east-1.amazonaws.com" -> null

Do you really want to destroy all resources?
  Terraform will destroy all your managed infrastructure, as shown above.
  There is no undo. Only 'yes' will be accepted to confirm.

  Enter a value: yes

aws_s3_bucket_acl.website: Destroying... [id=melearning.tk,public-read]
aws_s3_bucket_policy.website: Destroying... [id=melearning.tk]
aws_s3_bucket_website_configuration.website: Destroying... [id=melearning.tk]
aws_s3_bucket_acl.website: Destruction complete after 0s
aws_s3_bucket_website_configuration.website: Destruction complete after 1s
aws_s3_bucket_policy.website: Destruction complete after 1s
aws_s3_bucket.website: Destroying... [id=melearning.tk]
aws_s3_bucket.website: Destruction complete after 1s

Destroy complete! Resources: 4 destroyed.
```
</details>
