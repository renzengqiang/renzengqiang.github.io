---
layout: post
title:  🔍观察细节
categories: diary
---

🤔I think this should be a good start.: )


以前写代码很少会去考究比较细节的地方，昨天下并行计算课的时候，老师还问我，写过那么久的代码，那我的继续学习动机是什么？  
其实虽然写了很久的代码，但是我却是一个眼高手低，很少会花功夫去为几毫秒甚至几秒变得特别较真的人  
继续学习呢，给了我足够的时间和足够的资源，去把之前忽略的一部分细节收拾一下  
今天的 NC 实验就我关心的一些问题和 TA 小哥哥聊了很多，简单用一个示例记录之  
I think this should be a good start.: )

{% highlight python %}
def linear_merge(list1, list2):
    '''
    treat it as merge sort
    '''
    list1_index = 0
    list2_index = 0
    result = []
    
    while (list1_index <= (len(list1) - 1) or list2_index <= len(list2) - 1):
        if list1[list1_index] < list2[list2_index]:
            result.append(list1[list1_index])
            list1_index += 1
        elif list1[list1_index] == list2[list2_index]:
            result.append(list1[list1_index])
            list1_index += 1
            result.append(list2[list2_index])
            list2_index += 1
        else:
            result.append(list2[list2_index])
            list2_index += 1
            
        if list1_index == len(list1):
            result = result + list2[list2_index:]
            break
        if list2_index == len(list2):
            result = result + list1[list1_index:]
            break
    return result

def liner_merge2(list1, list2):
    '''
    use sort()
    '''
    result = list1+list2
    result.sort()
    return result

def liner_merge3(list1, list2):
    result = []
    while len(list1) != 0 and len(list2) != 0:
        if list1[0] <= list2[0]:
            result.append(list1.pop(0))
        else:
            result.append(list2.pop(0))
    return result+list1+list2

def liner_merge4(list1, list2):
    result = []
    head1 = 0
    head2 = 0
    while len(list1) - head1 != 0 and len(list2) - head2 != 0:
        if list1[head1] <= list2[head2]:
            result.append(list1[head1])
            head1 = head1 + 1
        else:
            result.append(list2[head2])
            head2 = head2 + 1
    return result+list1[head1:]+list2[head2:]
{% endhighlight %}

so  
what's the difference between all of these four funcs?  
明天继续更  
// 先打个时间戳  Oct 11, 19 21:29

