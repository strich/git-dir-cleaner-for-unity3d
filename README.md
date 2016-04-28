# Git Directory Cleaner for Unity3D
_A Git hook for Unity3D projects to automatically remove empty directories._

One of the few major annoyances one has with using Git with Unity3D projects is that Git doesn't care about directories and will happily leave empy directories around after removing files from them. Unity3D will make `*.meta` files for these directories and can cause a bit of a battle between team members when Git commits keep adding and removing these meta files.

Add this Git post-merge hook to the `/.git/hooks/` folder for repositories with Unity3D projects in them. After any Git pull/merge, it will look at what files have been removed, check if the directory it existed in is empty, and if so delete it.
