Description
Do you know how to use the web inspector?
Additional details will be available after launching your challenge instance



Guide:Upon entering the site, we will be greeted with the following directory called index.html and upon further navigation you can find other page namely about.html and contact.html which is shown below:
![index-html](https://github.com/user-attachments/assets/2efd2550-e28a-44db-8ffb-e7f58c41932d)
image for index.html

![about](https://github.com/user-attachments/assets/4670d7fc-585f-41d9-9860-da990d995d91)
image for about.html

![contact](https://github.com/user-attachments/assets/46e4e13c-c858-43cb-aae2-b041ba2a6f06)
image for contact.html

Inspecting the web content, i found nothing interesting beside its encourage me to nagvigate,search and inspect the website in which i did and i found something interesting in about.html
![about (2)](https://github.com/user-attachments/assets/ffe4b1b9-2e27-48ba-8dca-e3caedcd9f19)

The following code i pay attention to because the "notify_true" attribute because it don't have any interactable function in the web but also contain a weird string which i suspect is base64 encoding.
<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZjZmNmI3OGF9">

After that, i copy the string and paste it in an encoding identifying website to confirm my suspicion
![base64](https://github.com/user-attachments/assets/a899deaa-235d-4129-90bf-4c1f63b5d595)

After that i simply use an online tool like base64 decoder and decode it 
![answer](https://github.com/user-attachments/assets/96e4e8f1-cf5c-4660-bc7b-a562086386a5)

And it reveal the answer for this challange: picoCTF{web_succ3ssfully_d3c0ded_f6f6b78a}

In my opinion, this is a pretty straightforward challenge where it teach us to pay more attention to detail and not treat anything on the surface level in which i think can lay a good foundation for anyone focusing on this career.
