# TAR AND UNZIP 

## Compress file 

### Creating an simple archive

- `tar -cvf output.tar /path/input` :
    - `-c` will create an archieve
    - `-v` will enable verbose mode & will show the prograss  
    - `-f` allow us to name the archieve
### Createing an tar.gz archieve

- `tar -cvzf output.tar.gz /path/input`

### Creating an bzip2 archieve 

- `tar -cvjf output.tgz2 /path/input`

### Creating an archieve excluding some files/directorys 

- `tar -cvf output.tar /path/input1 --exclued=/path/input/exclued_file --exclued=/path/exclude_directory`





## List of files 

- `tar -tvf output.tar`
- `tar -ztvf output.tar.gz`
- `tar -jtvf output.tar.gz2`




## Decopress file

- `tar -xvf output.tar`
- `tar -zxvf output.tar.gz`
- `tar -jxvf output.tar.gz2`

- `unzip xxxx.zip -d /somedir`