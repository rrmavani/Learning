* [Create Basic Unit Test File](#Create_Basic_Unit_Test_File)
* [Modify Docker compose](#Modify_Docker_compose)

## Create Basic Unit Test File
Go to your code and create test folder structure
```bash
$ mkdir spec
$ cd spec
/spec$ mkdir unit
/spec$ cd unit/
/spec/unit$ vim page_spec.rb
```
Write test
```ruby
require 'capybara'
require 'capybara./dsl'

describe "Example page render unit tests" do
  it "Shows the Explore California logo" do
  end
end
```
## Modify Docker compose
```docker
  unit-tests:
    volumes:
      - "$pwd:/app"
    build:
      context: .
      dockerfile: rspec.dockerfile
```
<details>
  <summary>Full File</summary>
  docker-compose.yml

  ```docker
  version: '3.7'
  services:
    website:
      build:
        context: .
      ports:
        - 80:80
    unit-tests:
      volumes:
        - "$pwd:/app"
      build:
        context: .
        dockerfile: rspec.dockerfile
  ```
</details>
