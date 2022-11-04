# How to use GIT

1. Initiate
   1. Create a folder
   2. Right click, Open with Code
   3. Click 'Source Version Control' (3rd icon on the left)
   4. Click 'Initiate Repository'
2. Add file
   1. Add file to folder
   2. When you save a new item to the folder, there would be a notification at the Source Control section
3. Open Github Desktop
   1. Menu - File - Add Local Repository
   2. Put the location of current project
4. Upload the file to Stage
   1. Right click the file that we need to upload to Stage at the Source Version Control.
   2. Click the Staging the changes, or the plus icon
5. Commit
   1. Write the commit message, and press Ctrl + Enter or Check mark on the top row
6. Check the commit history through Github Desktop
   1. The commit log can be checked at History
7. Cancel the changes
   1. Right click the file, click the cancel the changes
   2. Then the file will be changed to previous commit
8. Save at the Repository
   1. At Github Desktop, Repository - Push
   2. Put the name of the Repository and hit the Publish Respository.
   3. Github will be create the repository automatically, and upload the local storage's code.
   4. Github website - Repository - Code

# Git의 파일 추적 방법

- 소스코드의 저장공간을 3가지로 분할

* Working Directory : Local storage
* Stage : Temporary Storage for selected files (that we trying to manage the version) from Working directory. Only items at Stage will be apply to commit
* Repository : Actual storage

When we initate, Git will be recognize every files in the Working Directory as a 'Untracted', and when user select the files that they want to track, then the file will change to 'tracked' status.
The files in Tracked status will be uploaded to Stage.

Stage, a temporary storage for managing the version of the file, includes the infos about files at the time of when user ask the files for tracking.

If the tracked files got modified, then the difference would be occured between the Working Directory and Stage. In this case, Git delete the file from the Stage

### How git tracks files?

- Git understands the files which got modified while it's on Stage, as Modified, while not got modified as Unmodified
- The modified files will be disabled from the Stage, so we need to uploade to Stage again after we edit it
- Only the files in the Stage will be uploaded to Repository

### Commit, the way Git tracks the file

When we want to write down the files on Stage as a specific version, we can use 'commit'
Commit enrolls the files on Stage as a new version
The changes which is committed will be record on Repository permanently

- Commit : Save permanently the infos about files which is on the Stage.
- Commit only saves the changes(EDITED parts from the previous version) which is came from the previous file to new files, not the whole file. So, Commit is created based on from previous commit

### At first, file starts as Untracked, cuz Git is not gonna track EVERY Files.

### When the user asks the tracking a specific file, its status will be changed to TRACKED, and it will be uploaded to Stage

### But when there is a change on the file which is located at the Stage, its status will be changed to MODIFIED

### Modified files is needed to be uploaded to the Stage by user when it needed to be saved.

### The files on the Stage, can be saved permanently by COMMIT
