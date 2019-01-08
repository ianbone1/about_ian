*Recover a file from git*

To restore a deleted file from your repo:

Scenario setup:

```
touch delete.me.recover.me
echo "This is my test file to delete and then restore" >> delete.me.recover.me
git add .
gst
git commit -m "Added test file to recover"
git push
git pull
```

Delete file and sync

```
rm delete.me.recover.me
git add .
gst
git commit -m "Deleted test file"
git push
git pull
```

To recover the file, you need the first 7 digits of the hash header where the file existed, get this from `git log`

```
git log
```

Sample output:
