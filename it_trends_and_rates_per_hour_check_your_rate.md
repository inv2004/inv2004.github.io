# IT trends and rates per hour - check your rate
https://github.com/inv2004

# Preamble

It happened recently that I had a reason to check upwork again. About 5 years ago I did it first time because I was so tires about enterprise and Java and I was trying to make a decision from boring, but pretty well payed tech, to intersting, but mostly hobby and non payed tech

# Dataset
With the respect to readers who are not interested in the technical process you can scroll to Conclusion section

I did search in IT category and found that it contains about~5000 offers. It was about 100 pages with 50 items per page, I went through the hundred pages and saved .har file in chrome, split it by page request and saved into separate files. Here comes the data for analysis.

You can find the most trending tags counted from each offer:

![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/e44ece5c-46a2-4087-8eee-efc38ed47ef8)
*select count(1) by tag from t*

As we can see, DevOps is the trending topic at the moment. Pretty funny, considering that just a few years ago I partly joined to DevOps team at one of the biggest banks in Europe, and my manager could not explain what "DevOps" means exactly. But now it is a top-trend.

Rates per hour seemed visibly lower than I expected. After a little investigation I found a lot of offers with much lower rates than usual. I can even remember some regions to dump rates before. Which is usual — you search other regions for rates equal or even higher than those in your region. So I filtered out those with dumping rates judging from my location.

Here is that I have in the final:

![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/a606ab67-709d-4064-8bc8-6a3a915eba7d)
Illustration: *select cnt:count(1), avg:0.5*(min+max), min: sum(min)/cnt, sum(max)/cnt, sum(price)/cnt by tag from t*

Only top 47 niches are listed here. Here's some explanation:

*Min* and *Max* are averages of minimum and maximum rates respectively (where the rate is specified), *Avg* is an average of the *Min* and *Max*. *Prj Price* is an average of fixed project prices, which is rather insignificant due to it's unrelatedness to work duration.

# Relations
I did a simple thing: I linked tags from the same offer, where center force of a node is a number of it's links. What was even harder, is to find a good graph-creating online tool.

[cosmograph.app](http://cosmograph.app/) proved that our IT is alive and rotates it's orbit around SQL

![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/4cae6655-2661-4588-859f-a323e428efe2)
Illustration: *IT is alive*

I generated the graph in graphviz. Too many minor links made the distribution rather ugly, so I limited a node with >=75 of them

![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/74ef98c9-fbbc-4fcb-bf08-3346248949a3)
Illustration: *Apologies for a nerdy look of the graph.*

To explore it in better detail, you can find it here [](https://raw.githubusercontent.com/inv2004/inv2004.github.io/main/it_trends_and_rates_per_hour_check_your_rate.svg)

From the point it is possible to see that DevOps the days mostly means DevOps for AWS, Docker and CI/CD, Python is the main dev language for devops also,

You can find two clusters here, second on is about Security, I am not sure I know the major diff between information/network and other security problems. Also, it is necessary to keep in mind that upwork contains a lot of "security" stuff like "hack my ex's instagram"

I would also like to detect another clusters, but, like I mentioned, I did not find good tools I can do it fast. Also, it was pretty clear that it is possible to merge some nodes like "AWS" and "Amazon EC2", but did not want to spend too much time on it

# Conclusion

In the end I created a table with the tags I think the most interesting and, especially the most interesting topic for me - programming languages:

![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/03c330d5-3a9a-41c2-b328-7dc5b3de3694)

From the table and graph it is pretty clear that DevOps goes hand to hand with AWS, sometimes it goes with Azure and it is payed a bit better. Knowledge of Docker is must-have If you want to work in DevOps. After that, K8s and TerraForm could also extend your feeding ground. "DevOps" contains "Dev" — this usually involves Python, Ansible would also help.

Programming languages is the most interesting topic for me personally.

Python is language for everyone, for tooling and not only. JavaScript is also high, but I am surprised with the rate I see. Next surprise for me is unreasonable (sorry) PHP with reasonable price for it. Java had some stagnation (from my perspective also) about 10 years ago, but it is still popular. C# is the half of Java. C++ is still good for the aged technology. Typescript - I think it should be merged with JS. Flutter looks not very popular, but I have to say that the amount of offers with it is pretty low, which might've caused bad values in rate. The same is applicable to C, but I actually thought C would be higher.

When I decided to quit Java I put my bets on Golang - mature enough for real work, was increased in popularity, but I have a feeling that it is ~ on the same level it was before. Maybe, if I were brave enough - I would invest into AWS the moment I made the decision. At least it looks reasonable from the current market.

Rust is mostly supported by crypto, but it is observable on the market which is a good result. Kotlin is a bit higher than Rust, and surprisingly I found that it is backed by backend more than by Android, like it was positioned before.

Databases. MySQL is the first database, which is expected — the number one database for those unwilling to to choose database. Postgres is the next one, Mongo, Redis. Unfortunately Clickhouse is nearly invisible, but I keep following interesting projects involving it.

# Prologue

This analysis is based on freelance exchange, but the results are still applicable for the employed. Of course, you can find some banks still use rare and aged technologies like APL (❤️) or Fortran, and it is a common scenario to stick to one of the departments for many years. It could be interesting and even profitable but not always good from job security perspective. If you are still choosing — this article might help you make a decision based on different criteria: to find the most profitable tech or tech which you could improve your skills. You can also put yourself on a scale from minimum to maximum rate based of your level and find out if you are payed reasonably or not, and, maybe it could help you into the fields of freelance, which could be profitable, but could be more risky also.

# PS: For non-IT:
![image](https://github.com/inv2004/inv2004.github.io/assets/4949069/55c323c4-7f01-428c-864a-8d99d5da6b4f)

