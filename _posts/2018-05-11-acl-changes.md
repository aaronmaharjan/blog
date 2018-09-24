---
layout: post
title: ACL_Changes
date: 2018-05-11 20:01 +1200
---

There have been a lot of Changes on ACL, the whole directory has been rewired.

The reason for this was the old file sturcture that we were working with leftover to us from the Software Engineering team wasn't efficient for us and we had to replicate a lot of code. The new Approach should let us bypass that by using includes to add blocks of code instead of having the whole bunch of code there.

Here is the old File structure:

<img src="/resources/acl_old.png" alt="old_acl_file_structure" height="1000" width="500">

As you can see there is no modularity and all the files are scattered and this would only become a growing problem as the number of files increase.

Here we have the new file structure which is much easier to navigate and also has a lot less repitition in the code.

<img src="/resources/acl_new.png" alt="new_acl_file_structure" height="1000" width="500">

This change was pushed by Adon, Even though we were already halfway through the semester It still seemed that we would be better off making these changes and catching up.. taking 5 steps back to make 10 leaps forward. After these changes I found it much easier to navigate when inspecting the files and code.
I Also lent a hand for when the team got stuck with DIRs as we were working with a completely new file structure. We managed to resolve the issue.

I read through the dirname manual found at: http://php.net/manual/en/function.dirname.php

and found out that the issue was with how we were trying to go back to a higher level in the directory. I found a non php solution after meddling with some code using basic html

{% highlight html %}
../../Image/my_Image.png 
{% endhighlight %}