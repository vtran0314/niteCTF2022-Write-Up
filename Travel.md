 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209477964-4f50435a-335a-48ca-ba45-e5f36a8bdea5.png">
</p>

Download the file I got the picture of an owl.

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209477979-782fd095-2ac1-4bba-8c40-4eddaaf00751.png"
</p>

Before deep dive into extract anything from the image, I used the strings command. Here, I found an suspicious URL 'bit.ly/mytodooolist
 
  <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209477984-2208ce10-5686-4408-967f-86d008d642ed.png">
</p>
  
 
Following the webpage I found a bunch of sticky note on the Jamboard.
 
  <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478132-3872d9c8-024f-46d1-b1eb-4877694897da.png">
</p>
 
 
I tried to inspect the website to look for any clues and I noticed that the word before is highlighted differently than the other so I took a closer look, then I found another url lead to another website.
  <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478138-74a9d118-6e41-4d77-8b43-24c966d30b97.png">
</p>

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478144-619ed23d-ffb6-47b5-9cf1-0951f45e2e68.png">
</p>
 
Follow the URL, it seem like a webpage of a restaurant

 <p align="center">
  <img src="">
</p>

Inspect the source code I found the following message:
 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478231-38950055-8df9-4fc7-8ae5-b573741a4834.png">
</p>

When I saw the word go back in time I thought about the WayBackMachine, so I spent a good amount of time on the website. Then I search for the source code that have the menu on it but no veil. 
So I thought, how about just put the tr4v3l1 to github and see what I could find. Indeed I found something interesting.
 
 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478236-3a62af39-5776-4ae1-aac3-a8df73e000a5.png">
</p>

At this point I thought I my job done here but it was blank. So I had to look deeper into this. So I noticed that there were 7 commits in this github repo. 

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478241-8f59ea8c-8188-439d-887c-d915522cd7e7.png">
</p>
  
Click on the commits I saw the flag file was updated on Dec22 so I click on it, and the file was empty again.

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478249-1522f1a0-b8f8-4e6c-acb5-073a2acae4ca.png">
</p>
 
I then look at the other commits; finally I found the flag in the website commit

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478261-684a8c0b-2f47-43bd-89c2-6d1a37f860a4.png">
</p>
 
#### Flag: nitectf{y0u_w3nt_b4ck_1n_t1m3}
