# python-data-assignments

# 1. Topic
# MeToo on Weibo

# 2. Data Source
# This dataset contains 431 microblogs on Weibo with "米兔运动" as the keyword.

# 3. Data fields
# Name - String e.g.niceyoonalim
# Time - String e.g.10-05
# Content - String e.g. 有些人总是爱把对错善恶与某个集体甚至与国家民族挂钩，学校出了丑闻了，不急于惩罚制裁施暴者，反倒先对受害者指指点点🙃“你现在把这件事公开，闹大了怎么办，学校对你不好吗🙃”都多久了，我们一个西方文论老师还在课堂上说“现在的中文系堕落了，那么多人参与了米兔运动”
# Repost - String e.g.0
# Comment - String e.g.1
# Like - String e.g.3


#4. Data Volume
#431 rows * 6 columns

#5. License
# CC 4.0

#6.Obstacles and solutions
# I had trouble locating the tag of elements I wanted at first. However, with the help of TA, I changed xpath into css_selector and successfully crawling the number of reposts, comments and like.


#7.Future work
# For a thorough analysis, I am going to enrich my dataset by crawling microblogs which are searched with more keywords related to MeToo.

#8. Reference 
# https://github.com/hupili/python-for-data-and-media-communication/blob/master/scraper-selenium/Weibo.ipynb 
