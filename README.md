# My Notes
 ## Basic commands:
- make directory
```
mkdir
```
- change directory
```
cd
```
- new item
```
ni
```
- list of contents
```
ls
```
 
 ## cURL commands:
  - curl  stands for client URL.
  - The following command will help us to extract all text from the given url
  ```
  curl "url"
  ```
  **Note:** use this command if any problem faced with curl
  ```
  [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
  ```
  - Extract data and store it in a file_name(data).txt file
  ```
   curl "url" -O data.txt 
  ```

  ## processing the text data extracted from the url:
 - Transform each space into a retun character
 ```
 tr ' ' '\12' < data.txt
 ```
 - Sending the output of the above command as input to sort command
  ```
 tr ' ' '\12' < data.txt | sort 
 ```
 - Sending the output of the above command as input to the command which counts the unique occurances of words
  ```
 tr ' ' '\12' < data.txt | sort | uniq -c
 ```
 
 - Sending the output of the above command as input to the command 
  ```
 tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr 
 ```
 - Getting help with sort flags
  ```
 sort --help 
 ```