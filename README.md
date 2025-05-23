## Overview

Merge multiple Mozc UT dictionaries into one and modify the costs.

## Press the Star button on GitHub

They need more Stars.

mozc: [1930 Stars](https://github.com/google/mozc)

fcitx5-mozc: [82 Stars](https://github.com/fcitx/mozc)

merge-ut-dictionaries: [40 Stars](https://github.com/utuhiro78/merge-ut-dictionaries)

> Starring a repository also shows appreciation to the repository maintainer for their work. - [GitHub Docs](https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars)

> リポジトリに Star を付けるということは、リポジトリメンテナに対してその作業についての感謝を示すことでもあります。- [GitHub Docs](https://docs.github.com/ja/get-started/exploring-projects-on-github/saving-repositories-with-stars)

## License

- mozcdic-ut.txt (generated by merge-ut-dictionaries): Combined

- [jawiki-latest-pages-articles-multistream-index.txt](https://dumps.wikimedia.org/jawiki/latest/): [CC BY-SA](https://ja.wikipedia.org/wiki/Wikipedia:ウィキペディアを二次利用する)
  - merge-ut-dictionaries use it to generate the costs for words.

- [dictionary*.txt and id.def](https://github.com/google/mozc/tree/master/src/data/dictionary_oss) from Mozc: [BSD-3-Clause](https://github.com/google/mozc)
  - merge-ut-dictionaries use them to remove duplicate words and update ID.

- Source code: Apache License, Version 2.0

## Download

```
git clone --depth 1 https://github.com/utuhiro78/merge-ut-dictionaries.git
```

## Configure

Comment out unnecessary dictionaries in src/merge/make.sh.

Default settings:

```
#alt_cannadic="true"
#edict2="true"
jawiki="true"
#neologd="true"
personal_names="true"
place_names="true"
#skk_jisyo="true"
sudachidict="true"
```

## Build

```
cd src/merge/
bash make.sh
cat mozcdic-ut.txt >> ../../../mozc-master/src/data/dictionary_oss/dictionary00.txt
```

Build Mozc as usual.

## Option: Generate the UT dictionaries using the latest stuff

Uncomment ```#generate_latest="true"``` in src/merge/make.sh.

It downloads the latest "jawiki-latest-pages-articles-multistream.xml.bz2" (4.1 GB).

## Option: Generate user dictionary files

Uncomment ```#generate_user_dictionaries="true"``` in src/merge/make.sh.

This tool converts the generated dictionary into several files that you can import as a user dictionary directly, without rebuilding mozc. However, adding the dictionary at compile time generally yields better results, so prefer that approach if possible.

## Dictionaries

Mozc UT dictionaries contain the following dictionaries:

* [mozcdic-ut-alt-cannadic](https://github.com/utuhiro78/mozcdic-ut-alt-cannadic)

* [mozcdic-ut-edict2](https://github.com/utuhiro78/mozcdic-ut-edict2)

* [mozcdic-ut-jawiki](https://github.com/utuhiro78/mozcdic-ut-jawiki)

* [mozcdic-ut-neologd](https://github.com/utuhiro78/mozcdic-ut-neologd)

* [mozcdic-ut-personal-names](https://github.com/utuhiro78/mozcdic-ut-personal-names)

* [mozcdic-ut-place-names](https://github.com/utuhiro78/mozcdic-ut-place-names)

* [mozcdic-ut-skk-jisyo](https://github.com/utuhiro78/mozcdic-ut-skk-jisyo)

* [mozcdic-ut-sudachidict](https://github.com/utuhiro78/mozcdic-ut-sudachidict)

[HOME](https://ss1.xrea.com/linuxplayers.g1.xrea.com/mozc-ut.html)
