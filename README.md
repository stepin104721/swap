# swap
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/6ea8b6e3304e4c3e9deaa6f7650aaded)](https://app.codacy.com/manual/stepin104721/swap?utm_source=github.com&utm_medium=referral&utm_content=stepin104721/swap&utm_campaign=Badge_Grade_Dashboard)
name: cppcheck-action
on: [push]

jobs:
  build:
    name: cppcheck
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        
      - name: Install cppcheck
        run: sudo apt-get -y install cppcheck
      - name: Cppcheck code
        run: cppcheck
