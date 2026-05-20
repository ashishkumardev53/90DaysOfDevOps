Linux File read and write – Day 06

Practiced basic file read/write using core Linux commands.
Kept it simple and repeatable.

What I did

touch notes.txt

echo " how are you" > notes.txt

echo " where are you" >> notes.

echo " iam fine" | tee -a notes.txt

cat notes.

head -n 2 notes.

tail -n 2 notes.txt
