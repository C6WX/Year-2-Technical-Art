# Week 7-10 - Asset Requests

**Callum Wade** **2404781** **12/11/25** 

**Client: Cameron Gildea**

**[Request Document](https://ucreative-my.sharepoint.com/:w:/g/personal/2322268_students_ucreative_ac_uk/EdvLvx6UqlpMqSFkGqqkYycBbzzZW3iyfWnn-7DaSxcnPA?e=P9hHvU)**

## Client Communication <!-- S&G checked --> 
Whenever something wasn't clear from the request form, I emailed Cameron to clear up what was required of me. The main thing that I needed to ask about was the checking which style of visual effects or animations he preferred. An example of this is with the ripple effect. I created a two different effects based on the request he asked for and then asked for feedback on which one he preferred and if there was anything that he would like changing. Also when it came to the throw animation, I found two animations that I felt work well for the final throwing animation, one where the character thrusts their hands forwards in a ball-shaped form (this animation worked the best and worked well with the start and charge up animation), and another where the character throws from over their head, which fit the client's description the best.
<br>
The main challenges that I felt came up with communication between me and my client was mainly due to the time I had to wait for a response. As a lot of my emails were sent to ask for feedback, a long delay before getting a response meant that I couldn't always continue with what I was working on for quite some time. As a result, I would move onto something else to keep me busy but this normally lead to me doing too many things at once. An example of this is when i created both of the ripple effects, I sent an email with both of them in but as I couldn't just directly speak to or message my client, it took a while to get a response so I ended up moving onto the crack effects. When it came to this, I didn't find it a problem to be doing the ripple effects and cracks at the same time, but it mainly became difficult while I was waiting for a response while creating the animations as I was working on the movement animations, the jumping animations, the combat animations, and the rock throw animations all at once. However, the delay before I received a reply to my emails were not the fault of my client as he did say that he was working quite a lot which I could definitely understand and relate too.
<br>
One thing I found to be a challenge but also a benefit was writing professionally within the emails I sent. Writing professionally is not new to me at all, but it is a lot different to how I normally message Cameron so it definitely took some getting used to. However, I felt that it created a separate professional relationship between us that helped communication between us when discussing the requested assets.

<!--
### Emails

#### 12/11/25

12:48pm

![1248](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/12%2048PM.png)
<br>

2:34pm

![234](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/2%2034%20PM.png)
<br>

5:14pm

![514](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/5%2014PM.png)
<br>

5:49pm

![549](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/5%2049PM.png)
<br>

6:03pm

![603](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/6%2003PM.png)
<br>

7:42pm

![742](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/12%2011%2025/7%2042PM.png)
<br>
<br>

#### 18/11/25

10:51am

![1051](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/18%2011%2025/10%2051AM.png)
<br>
<br>

#### 21/11/25

12:43pm

![1243](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/21%2011%2025/12%2043PM.png)
<br>

3:33pm

![333](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/21%2011%2025/3%2033PM.png)
<br>

4:22pm

![422](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/21%2011%2025/4%2022PM.png)
<br>

4:58pm

![458](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/21%2011%2025/4%2058PM.png)
<br>

5:52pm

![552](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/21%2011%2025/5%2052PM.png)
<br>
<br>

#### 22/11/25

2:44pm

![244](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/22%2011%2025/2%2044PM.png)
<br>
<br>

#### 25/11/25

4:33pm

![433](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/25%2011%2025/4%2033PM.png)
<br>
<br>

#### 26/11/25

1:48pm

![148](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/26%2011%2025/1%2048PM.png)
<br>

6:36pm

![636](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Professional%20Practice/26%2011%2025/6%2036PM.png)

-->

## Technical Problem-Solving
When creating the plugins, I has quite a few problems with the multiple plugins I was creating. At first I tried to make the ripple effect plugin by advanced copying all the files needed for the effect and the test map into the new plugin. For the test map I was going to have a combat enemy from the combat Unreal Engine variant, so I copied all the combat files into the plugin too. When I tested the test map in the original project, it worked perfectly fine, the player would spawn, they would attack the enemy and the enemy would die and spawn the ripple effect. However the problem arose when I tested it in a new project. After loading the test map, the combat enemy wouldn't spawn and neither would the effect. I also received multiple error messages saying that I was missing files. After checking what the error messages wanted, it turned out that the files it was missing were in the project, but it wanted them to be in different places to were they were. To fix this, I moved the ripple material to the exact file it wanted. Unfortunately, the second missing file was for the combat enemy, which it wanted to be outside of the plugin in a specific folder, like the original combat enemy was in my main project. I could've easily fixed this by creating that folder but that would mean that my client would have to mess around with the folders when they wanted to import the plugin. Because of this, I moved onto the next plugin and tried another method.
<br>
Instead of advanced copying the files into the plugin folders, creating multiples of the same file, I tried just moving the original files directly into the plugins which would mean that the only thing changing would be the directory of each file, not the file that each one now has to reference. Doing this would would solve the previous problem I had as there would be no files that are expecting a file they are referencing to be somewhere else. I once again created a test map and tested the plugin in a new project. This time I received a blueprint error. In each one of my blueprints, every single reference had been reset to none. This would mean that I would've had to set all the references again to test it and that my client would have to do the same thing. To try and fix this problem, I repackaged the plugin and made sure my importing method was correct, but that didn't work. So I then tried using the update redirector references feature in Unreal Engine, but it did nothing and I still had the same error. Due to this error happening a week before the client deadline, I decided to send my client my whole project instead of plugins so that they had enough time to implement the assets they requested.
<!--CONTINUE WORKING ON THIS-->

## Workflow & Time Management<!-- S&G checked --> 
When it came to time management during this project, I felt like I had lots of room for improvement, but at the same time I felt like I did really well with the time I was given and the time I get to work on it. The main thing I would improve is the fact that I didn't use any form of time manager such as Trello. This is because I normally prefer to work on whatever I feel is most important first and then I work on it whenever I am able to until I have finished it or am unable continue, then I will move onto the next asset. Using a time management application would have likely helped me get things done at a better pace than I did but I normally prefer to work free from lots of small deadlines and instead just focusing on the main deadline since I don't have much time to get work done at the moment so I feel like I would miss the small deadlines. 
<br>
The first thing I did when starting this assignment was break the request form down into all the parts my client wanted made and then I got started on the ripple effect. After making two different effects to give my client a choice on which he preferred, I sent them to him via email and while waiting for a response, I moved onto the next thing. Normally after receiving feedback, I would finish the part of what I was working on and go back to what I was doing if major changes were required, like with what happened with the crack effect as photoshop ruined it's parallax occlusion mapping. This method isn't the best but has always worked for me as it feels natural while im working. I feel like this is where a time management application would have helped the most as it would have kept me more focused on one thing at a time. However a time management application doesn't account for waiting for responses from a client so it has its positives and negatives.

## Professional Practice<!-- S&G checked --> 
The main thing that you learn straight away when working with a client is that you aren't the only one relying on you to get this work done. Realising that you have an even earlier deadline than normal since your client needs the assets much earlier than the deadline can add pressure when you're working for them but proper time management and/or putting the time in as soon as possible is the best solution for this. I managed to get all the work done on time and after looking at my work load and who my client was, the pressure was alleviated almost instantly as I knew the client and knew I could get the work done even though it was quite a lot.
<br>
As well as realising that you have someone relying on you, you also have to rely on someone else to provide constant feedback on what you have done as the work doesn't need to be a certain way for you, but for your client. As I discussed previously, the communication between myself and my client was really professional and helpful but waiting for responses could take a while, which is the main thing you realise when working for someone else as everyone else has things to do too. 
<br>
A challenge that arises when you have to deliver to the client's specifications is the fact that you both have different images in mind of what is wanted from each assets. I was given a well written request document with a collection of references but there is a very high chance that we still have different visions of what is being requested. This is where communication really comes in helpful as you can ask and discuss each topic. Even with discussing each asset, it is always likely that we still have different images in mind for what each asset should be and look like which is where the main challenge lies. If the client was to make the assets themselves, they would get exactly what they wanted, but when working with someone else, that is nearly impossible and that is expected - someone else is hired to save time not get it perfect.

## Quality vs Deadline: How did you balance quality with the project timeline?

