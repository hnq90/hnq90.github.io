# How to use Currently's Premium Themes for free?

To refresh my fat Chrome's new page, I switched from ["2day is a good day"](https://github.com/Code4Fap/2dayIsAGoodDay") (my extension 🤣) to ["Currently"](https://chrome.google.com/webstore/detail/currently/ojhmphdkpgbibohbnpbfiefkgieacjmh"). `Currently` impressed me at first look. It displays only time & forecast information, but it's enough for me.
After installing it, I found that I can choose some themes through `Options` page.
Besides two free themes: `Classic`, the old style from the previous version of `Currently`, & `Currently 2.0`, there are four themes which need paid to use.
Fortunately, I found a small trick which let us use premium themes for free 💩

#### Here's the instruction:

* Open `Currently` option panel 😎
![](/content/images/2017/03/Selection_192.png)

* Choose your favourite theme 😤
![](/content/images/2017/03/Selection_193.png)

* Open `Chrome Dev Tools` by pressing <kbd>F12</kbd>. 😲
![](/content/images/2017/03/Selection_194.png)

* Copy & paste this spell to `Console` tab 👻
```
document.querySelector('#themes-container > div > div > div > a.button.ng-hide').classList.remove('ng-hide');console.log('%cSUCCESS. Please click SAVE button.', 'background:#333; color:#fff; font-size:18px;');
```
And run it by pressing <kbd>Enter</kbd>.
![](/content/images/2017/03/Selection_195.png)

* A magical `Save` button has just appeared next to `Buy` button.
 Click it, press <kbd>F12</kbd> again to turn off `Chrome Dev Tools` and enjoy that premium theme 🤗

 ![](/content/images/2017/03/Selection_196.png)
 ![](/content/images/2017/03/Selection_198.png)

If you like this post, please feel free to spread it to your friends. Thank you so much 😻

PS: Sorry Currently Team 🤧
