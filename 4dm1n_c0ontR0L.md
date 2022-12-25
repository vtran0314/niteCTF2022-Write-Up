Description:

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478838-64ca647f-a019-46ed-aefa-59e69f88be90.png">
</p>

Webpage's look:
 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478852-748cdb34-ca2a-4e94-9800-14c72118a18e.png">
</p>

From the description, I knew this must related to SQLi that's why I thought so I go ahead and tested out the SQLi with [OWASP Zap Automated tool](https://www.zaproxy.org/download/).


Zap is pretty simple to use. I started it by giving it the url and click `Attack` button. It will use the library it have to attack the webpage. You can see in the picture below.

NOTE from ZAP: Please be aware that you should only attack applications that you have been specifically been given permission to test.

<p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478878-08ab5a94-b4ce-4810-acb2-7024d946561e.png">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209479817-831702b2-971c-425e-8ea0-b00ce8708c75.png">
</p>


While I was working on other challenges, I gave a quick glance to ZAP and I saw a return code 302 out of a bunch of 200. So I decide to take a look.

<p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478917-baea332f-c88b-4e07-acd9-21c720e25b92.png">
</p>

Its a redirect page from the input of SQLi. And looking at the response message of the 302 code, I could see that there is a button that I must click on to see something.
<p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209478936-10d2f276-7900-4a19-85d1-776bdfaec598.png">
</p>

I then the information that Zap used to attack the webpage, decoded the URL strings and used it as username and password. 

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209479153-6f6514ff-e2e6-4ea2-a061-f93ed1ebb1cf.png">
</p>

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209479582-4e54e060-d10e-4487-a311-c2bd5d3bec9f.png">
</p>

Finally, I got the flag.

 <p align="center">
  <img src="https://user-images.githubusercontent.com/106710730/209479312-a9940955-618a-4271-ba2b-1b422a336046.png">
</p>


####Flag: nitectf{w3nT_1nT0_Th3_s3rV3r}
