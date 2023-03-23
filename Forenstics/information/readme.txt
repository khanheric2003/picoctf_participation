Use Webshell then exiftool to read the information of the file

exiftool {filename} --> see description of file
exiftool {filename} | grep {part_of_the_description} --> seperate that part of the description < it will show "type        :  information"
exiftool {filename} | grep {part_of_the_description} | sed -e 's/.*: //' --> seperate the "type" and only leave the information
exiftool {filename} | grep {part_of_the_description} | sed -e 's/.*: //' | base64 -d --> translate it into base64 form

s