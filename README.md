Script run on OSX

# Requirements:
	brew install coreutils

# Get modified files:

1. Run this command to get the files-to-copy.txt file:
	./getmodifiedfiles <clean-folder-path> <infected-folder-path>

2. In files-to-copy.txt remove the unnecessary folder path prefix before every file

3. Copy the files-to-copy.txt file into the clean folder

4. In the clean folder, run:
	zip restore.zip $(cat files-to-copy.txt) -r

5. Overwrite the infected files with the zipped ones.

# Get newly create php files

1. Run this command to get the files-to-copy.txt file:
	./getnewfiles <clean-folder-path> <infected-folder-path>

2. In newfiles.txt remove the unnecessary folder path prefix before every file

3. On your server delete the files which are inside newfiles.txt