# clevetong.github.io
1. 每个主题表示什么意义？
通过鼠标悬浮在左边的气泡上，我们可以选择查看具体的某个主题。选定后，右侧面板会相应地显示出跟这个主题相关的词汇，通过总结这些词汇表达的意义，我们可以归纳出该主题的意义。

2. 但是，作者却不局限于此，右侧词汇都是跟主题相关，但是到底谁更相关呢？
在这里，LDAvis的作者提出了一个算法：
relevance(term w | topic t) = λ * p(w | t) + (1 - λ) * p(w | t)/p(w);
某个词语主题的相关性，由λ参数来调节。如果λ接近1，那么在该主题下更频繁出现的词，跟主题更相关；如果λ越接近0，那么该主题下更特殊、更独有（exclusive）的词，跟主题更相关。所以读者可以通过调节λ的大小来改变词语跟主题的相关性，至于λ取多少，读者可以自己多尝试。

3. 每个主题有多么普遍？ 
在跑完主题建模之后，我们就可以知道每个主题出现的频率。LDAvis的作者将这个数字，用圆圈的大小来表示，所以气泡的大小表示主题出现的频率。

4. 主题之间有什么关联？ 
这里作者用多维尺度分析，提取出主成分做维度，将主题分布到这两个维度上，主题相互之间的位置远近，就表达了主题之间的接近性。
