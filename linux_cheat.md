# Linux cheat sheet

open a file with default package
```bash
xdg-open .bashrc
```
# ssh
SSHFS folder share command, [remote location] [local folder to mount]
```bash
sshfs 192.168.0.83:/home/keir/catkin_ws ~/cat_sshmnt
```
Then to unmount:
```bash
fusermount -u ~/cat_sshmnt
```
to ssh in with graphics
```bash
ssh -X username@192.168.0.83
```
ssh and allow keys to be used - good for git stuff
```bash
ssh -A  aslab@husky-ph
```
sshcopy - move contents of current folder to remote computer home/pack_cal folder
```bash
sudo scp -r * gro166@192.168.2.38:pack_cal
```
# files and folders
list folder contents with file size and paemissions
```bash
ls -lh
```
change permissions - add execution rights
```bash
chmod +x wildcat.yaml
```
rename
```bash
sudo mv none_self_strike.yaml husky_self_strike.yaml
```
copy husky_self_strike.yaml in current folder to /etc/pack/slam/
```bash
sudo cp husky_self_strike.yaml /etc/pack/slam/
```
delete everything in the folder and subfolders begiinning with 2020_01_
```bash
sudo rm -r 2020_01_*
```
disk use - folder size
```bash
du -h
```
print working directory
```bash
pwd
```
difference between two files - esc then :q to exit vim
```bash
vimdiff ~/subt/src/subt_launch/config/husky/husky_behaviour_path_follow.yaml ~/subt/src/subt_launch/config/kitten/kitten_behaviour_path_follow.yaml 
```

# processes
list processes
```bash
ps aux
```
often useful with grep - gz is gazebo stuff
```bash
ps aux | grep gz
```
kill process 7648
```bash
kill 7648
```
kill process 7648 an do not allow it to be blocked
```bash
kill -9 7648
```
# tmux commands
start tmux
```bash
tmux
tmux new -s <session name>
```
this exits tmux
```bash
^d
```
tmux prefix key - tmux will interpret the keystroke following the prefix as a tmux shortcut.
```bash
^b
```
Panes split and navigate
```bash
^b %
```
```bash
^b <arrow key>
```
detach and reattach session
```bash
^b d
tmux ls
tmux attach -t <session name>
```
this gets you into scroll so you can use the arrow keys, mouse or pgup pgdn
```bash
^b [
```
quit scroll				
```bash
^b q
```
opens new tab
```bash
^b  c
```
moves to tab 1			
```bash
^b 1
```
