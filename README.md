# A experiment about script loading  

## Something about the experiment 
When I was preparing for the interview this autumn. I was always asked that  
> "Do you know the two properties of `defer` and `async` on the `<script>`? What are the functions of these two properties ?" 

Of course! There are so many answers on the forum, and  it is easy to get [the answer](https://zhuanlan.zhihu.com/p/292953374). But is it true? And that's why I start this experiment.  
In this experiment, I resort to the `Performance` in Chrome Devtool. Let's begin! 

# Normal
~~~html
<body>
    <h1>Script without defer or async</h1>
    <script src="./src/normal.js"></script>
</body>
~~~  
### some screenshots
> ![please config your DNS](./image/screenshots/1664510868(1).png)
___
> ![please config your DNS](./image/screenshots/1664510576(1).jpg)
___
> ![please config your DNS](./image/screenshots/1664511545(1).png)
___ 
> ![please config your DNS](./image/screenshots/1664517315(1).png)

### picture from forum 
> ![please config your DNS](./image/%E5%8D%97%E5%B1%B1%E8%A1%8C%E8%80%85%E6%96%87%E7%AB%A0%E6%8F%92%E5%9B%BE/script_normal.jpg) 


# Defer 
~~~html
<body>
    <h1>Script with defer</h1>
    <script defer src="./src/defer.js"></script>
</body>
~~~
### some screenshots 
> ![please config your DNS](./image/screenshots/1664512258(1).png)  
Between finishing parsing html and executing javascript code, there isn't `layout`,`paint` or `composite`. 
___ 
> ![please config your DNS](./image/screenshots/1664512838(1).png) 
___ 
> ![please config your DNS](./image/screenshots/1664517452(1).png)

### picture from forum
> ![please config your DNS](./image/%E5%8D%97%E5%B1%B1%E8%A1%8C%E8%80%85%E6%96%87%E7%AB%A0%E6%8F%92%E5%9B%BE/script_defer.jpg) 


# Async 
~~~html
<body>
    <h1>Script with async</h1>
    <script async src="./src/async.js"></script>
</body>
~~~
### some screenshots 
> ![please config your DNS](./image/screenshots/1664516693(1).png) 
___
> ![please config your DNS](./image/screenshots/1664516980(1).png) 
___ 
> ![please config your DNS](./image/screenshots/1664517544(1).png) 
### picture from forum 
> ![please config your DNS](./image/%E5%8D%97%E5%B1%B1%E8%A1%8C%E8%80%85%E6%96%87%E7%AB%A0%E6%8F%92%E5%9B%BE/script_async1.jpg) 
___
> ![please config your DNS](./image/%E5%8D%97%E5%B1%B1%E8%A1%8C%E8%80%85%E6%96%87%E7%AB%A0%E6%8F%92%E5%9B%BE/script_async2.jpg)  


