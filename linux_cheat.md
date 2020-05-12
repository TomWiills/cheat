


### open a file with default package
xdg-open .bashrc

------------ ssh ---------
### SSHFS folder share command, [remote location] [local folder to mount]
sshfs 192.168.0.83:/home/keir/catkin_ws ~/cat_sshmnt

### Then to unmount:
fusermount -u ~/cat_sshmnt

### to ssh in with graphics
ssh -X 192.168.0.83

### ssh and allow keys to be used - good for git stuff
ssh -A  aslab@husky-ph

### move contents of current folder to remote computer home/pack_cal folder
sudo scp -r * gro166@192.168.2.38:pack_cal


------------ files and folders ---------
### list folder contents with file size and paemissions
ls -lh

### change permissions - add execution rights
chmod +x wildcat.yaml

### rename
sudo mv none_self_strike.yaml husky_self_strike.yaml

### copy husky_self_strike.yaml in current folder to /etc/pack/slam/
sudo cp husky_self_strike.yaml /etc/pack/slam/

### delete everything in the folder and subfolders begiinning with 2020_01_
sudo rm -r 2020_01_*


### disk use - folder size
du -h

### print working directory
pwd

### difference between two files - esc then :q to exit vim
vimdiff ~/subt/src/subt_launch/config/husky/husky_behaviour_path_follow.yaml ~/subt/src/subt_launch/config/kitten/kitten_behaviour_path_follow.yaml 


--------------- processes------------------
### list processes
ps aux

### often useful with grep - gz is gazebo stuff
ps aux | grep gz

### kill process 7648
kill 7648

### kill process 7648 an do not allow it to be blocked
kill -9 7648

--------------tmux commands--------------
### start tmux
tmux
tmux new -s <session name>

### this exits tmux
^d

### tmux prefix key - tmux will interpret the keystroke following the prefix as a tmux shortcut.
^b

Panes split and navigate
^b %
^b <arrow key>

### detach and reattach session
^b d
tmux ls
tmux attach -t <session name>

### this gets you into scroll so you can use the arrow keys, mouse or pgup pgdn
^b [

### quit scroll				
^b q

### opens new tab
^b  c

### moves to tab 1			
^b then 1

---------git--------
### investigate
git status
git log
git diff

### diff between checkouts
### 7bed629b5a9864c97a226e448cc0a007cf0a1e6f - new
### fd3ec8c6a7353cde620ed7eeeb6b0e7e7644bbcd - old
### git diff old..new
git diff fd3ec8c6a7353cde620ed7eeeb6b0e7e7644bbcd..7bed629b5a9864c97a226e448cc0a007cf0a1e6f

### submodule sync
git submodule sync --recursive && git submodule update --recursive --init



