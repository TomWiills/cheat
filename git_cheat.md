# git cheat sheet
## investigate
```bash
git status
git log
git diff
```
## diff between checkouts
7bed629b5a9864c97a226e448cc0a007cf0a1e6f - new
fd3ec8c6a7353cde620ed7eeeb6b0e7e7644bbcd - old
```bash
git diff old..new
git diff fd3ec8c6a7353cde620ed7eeeb6b0e7e7644bbcd..7bed629b5a9864c97a226e448cc0a007cf0a1e6f
```
## make folder and clone
```bash
git clone --recursive 'https://github.com/EEEManchester/csiro-rad-avoid.git' ./src
git clone --recursive 'git@github.com:EEEManchester/mallard.git' ./src
```
## submodules
```bash
git submodule sync --recursive && git submodule update --recursive --init
```




