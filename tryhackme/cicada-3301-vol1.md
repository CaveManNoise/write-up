Hello, We are looking for highly intelligent 
individuals. To find them, we have devised a test.
There is a message hidden in this image
Download and unzip the folder given to begin
Good Luck
-3301
link https://tryhackme.com/r/room/cicada3301vol1 
upon download the file, we will have the following zip file
[Cicada_3301_1586991734089 (1).zip](https://github.com/user-attachments/files/17238791/Cicada_3301_1586991734089.1.zip)

Inside of it will be 2 files: 1 audio and 1 jpg. I tried to used steghide on the jpg file with no passphrase and yield no result so i think either there is nothing inside the jpg or i don't have the passphrase yet so i will focus on the audio file

Audio file: the content inside the wav audio file is very odd and listening to it, i can't found any recognizable pattern like morse code so i turn to a tool called sonic-visuallizer to analyze for anything like waveform or spectrogram which is likely

![sonic](https://github.com/user-attachments/assets/74a91bd7-4f37-4d34-a593-5c991547c198)

Nothing unusual to be found here in the waveform section so i turn on the spectrogram panel and found this QR code which indicate i am on the right track. 

![qr](https://github.com/user-attachments/assets/9d7c8416-a87d-4904-9ba3-905cb3df5ac4)

Scanning the Qr reveal the pastebin website (https://pastebin.com/wphPq0Aa?zarsrc=1303) and complete the question for task 1 and 2 of the puzzle

![pastebin](https://github.com/user-attachments/assets/d6c09204-b804-4d5d-bcdf-a6a09a9a732a)

Turning to task 3 of the puzzle require me to decode the passphrase and key that we just found in pastebin. Looking at both the passphrase and key, i suspect this can be classical cipher like ceaser cipher but the long string of text prove me otherwise. So i belive an online tool (https://www.dcode.fr/cipher-identifier) might help me in solving this.

![encode_indentifying](https://github.com/user-attachments/assets/1dbedf43-8418-4fc6-b614-e8e8767d9328)

Looking from the result of the indentifier, i doubt its be an youtube link because of it short length, rail fench becasue its key is needed in the form of numeber... which only left base64 or base62 as the remaining choice. I copy the key "Q2ljYWRh" (because it shorter and may prove to be provide a more precise result) into a base64 and base62 decoder and yield the following result


![false_answer](https://github.com/user-attachments/assets/52a2489c-e167-49c9-b5d0-313563d0956f)

Definitely not the base62 looking from the result which the base 64 is the only correct answer which can be observe below

![true_answer](https://github.com/user-attachments/assets/d443c7a7-8a91-4093-a9a3-d942d0c6bccd)

Result yielded from the passphrase look a bit weird but since there is no other way to go other than "base64" option so i have to go with this one and further decrypt it to see if it is true

![passphrase](https://github.com/user-attachments/assets/80439a62-ca55-4240-a11a-4717540aaa64)






