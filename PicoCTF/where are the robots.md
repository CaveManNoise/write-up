Description
Can you find the robots? https://jupiter.challenges.picoctf.org/problem/60915/ (link) or http://jupiter.challenges.picoctf.org:60915
Upon clicking on the website, i am greeted with the following image 
![index](https://github.com/user-attachments/assets/232d3d4b-24df-43d2-a4ef-a1af583266a2)

I inspect and check the source code but nothing can be found beside the webcontent asking me where the robot so i suspsect it probably mention robots.txt (an instruction file to any webcrawler and search engine) so i did and here the result
![robots txt](https://github.com/user-attachments/assets/afb00e8f-0cfe-46d4-a4ff-7fd248111229)

In the disallow section, it tell the bot not crawl the /8028f.html but the robots.txt unless specify normally doesn't stop user from manually entering it so i enter it and it reveal the flag i looking for
![answerr](https://github.com/user-attachments/assets/4d068967-ed10-4af2-85aa-955840ca4791)
answer: picoCTF{ca1cu1at1ng_Mach1n3s_8028f}



personal thought: A robots.txt file is a special file that website owners use to guide search engines, like Google, on how to explore their site. When a search engine visits a website, it looks for this file to see if there are any rules it should follow.However, i concern that many inexperienced developer may mistake it as a security tool because it only guide the bot where to look and crawl and not human user.
example: when a robots.txt of a website disllow "/admin", it will prevent any bot from entering that area but accidentally expose the existance of that place to any user curious enough to check the robots.txt and if no proper secrutiy method is applied, the risk of getting exploited is huge.
prevention: Use .htaccess to establish whitelist behiviors such as allowing only trusted ip to access the restricted area while combine with other methods such as honeypot techinque (Honeypot URLs: Create hidden links in your website that legitimate users won’t see, but bad bots will follow. Monitor these pages to identify bad bots or malicious crawlers and block them based on their IP address)

