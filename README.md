# Converting-TS-files-to-MP4
This following set of instructions help convert TS files to MP4 through built in Windows cmd features
thelegendaryzayd note

ffmpeg -i movie.ts -c copy -bsf:a aac_adtstoasc movie.mp4
**if file name has spaces write
ffmpeg -i "my video file.ts" -c copy -bsf:a aac_adtstoasc "my video file.mp4"

tutorial:
open cmd
copy and paste: ffmpeg -i
Then drag the .ts file into the terminal, it will paste the full path automatically.
then copy and paste: -c copy -bsf:a aac_adtstoasc output.mp4

example:
ffmpeg -i "C:\Users\zaydn\Downloads\Video\Spider-Man- Across the Spider-Verse.ts" -c copy -bsf:a aac_adtstoasc "C:\Users\zaydn\Downloads\Video\Spider-Man- Across the Spider-Verse.mp4"

for multiple files you will need to use a for loop command:

without spaces ex:
for %i in ("C:\Users\zaydn\Downloads\Videos\*.ts") do ffmpeg -i "%i" -c copy -bsf:a aac_adtstoasc "C:\Users\zaydn\Downloads\Videos\%~ni.mp4"

copy and paste: for %i in
then drag file into terminal
copy and paste: do ffmpeg -i "%i" -c copy -bsf:a aac_adtstoasc
then drag file
then copy and paste this after the file: \%~ni.mp4

with spaces ex:
for %i in ("C:\Users\zaydn\Downloads\book 2 earth\*.ts") do ffmpeg -i "%i" -c copy -bsf:a aac_adtstoasc "C:\Users\zaydn\Downloads\book 2 earth\%~ni.mp4"
