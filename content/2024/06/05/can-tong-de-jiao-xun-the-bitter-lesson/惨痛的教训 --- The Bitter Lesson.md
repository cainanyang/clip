---
title: "惨痛的教训"
date: 2024-06-05T13:36:30+08:00
updated: 2024-06-05T13:36:30+08:00
taxonomies:
  tags: []
extra:
  source: http://www.incompleteideas.net/IncIdeas/BitterLesson.html
  hostname: www.incompleteideas.net
  author: 
  original_title: "惨痛的教训 --- The Bitter Lesson"
  original_lang: en
---

## Rich Sutton 里奇·萨顿

### March 13, 2019 2019 年 3 月 13 日  

The biggest lesson that can be read from 70 years of AI research is that general methods that leverage computation are ultimately the most effective, and by a large margin. The ultimate reason for this is Moore's law, or rather its generalization of continued exponentially falling cost per unit of computation. Most AI research has been conducted as if the computation available to the agent were constant (in which case leveraging human knowledge would be one of the only ways to improve performance) but, over a slightly longer time than a typical research project, massively more computation inevitably becomes available. Seeking an improvement that makes a difference in the shorter term, researchers seek to leverage their human knowledge of the domain, but the only thing that matters in the long run is the leveraging of computation. These two need not run counter to each other, but in practice they tend to. Time spent on one is time not spent on the other. There are psychological commitments to investment in one approach or the other. And the human-knowledge approach tends to complicate methods in ways that make them less suited to taking advantage of general methods leveraging computation.  There were many examples of AI researchers' belated learning of this bitter lesson, and it is instructive to review some of the most prominent.  

从 70 年的人工智能研究中可以学到的最大教训是，利用计算的通用方法最终是最有效的，而且效率很高。其最终原因是摩尔定律，或者更确切地说是摩尔定律对每单位计算成本持续呈指数下降的概括。大多数人工智能研究都是在假设代理可用的计算是恒定的情况下进行的（在这种情况下，利用人类知识将是提高性能的唯一方法之一），但是，在比典型研究项目稍长的时间内，计算量会大大增加不可避免地变得可用。为了寻求在短期内产生影响的改进，研究人员寻求利用他们对该领域的人类知识，但从长远来看，唯一重要的是计算的利用。这两者不一定相互矛盾，但在实践中却往往相互矛盾。花在其中一个上的时间就是没有花在另一个上的时间。对其中一种方法的投资存在心理承诺。人类知识方法往往会使方法变得复杂，使其不太适合利用利用计算的通用方法。人工智能研究人员迟来的教训有很多，回顾一些最突出的例子是有启发性的。

In computer chess, the methods that defeated the world champion, Kasparov, in 1997, were based on massive, deep search. At the time, this was looked upon with dismay by the majority of computer-chess researchers who had pursued methods that leveraged human understanding of the special structure of chess. When a simpler, search-based approach with special hardware and software proved vastly more effective, these human-knowledge-based chess researchers were not good losers. They said that \`\`brute force" search may have won this time, but it was not a general strategy, and anyway it was not how people played chess. These researchers wanted methods based on human input to win and were disappointed when they did not.

  

在计算机国际象棋领域，1997 年击败世界冠军卡斯帕罗夫的方法是基于大规模的深度搜索。当时，大多数计算机国际象棋研究人员对此感到沮丧，他们寻求利用人类对国际象棋特殊结构的理解的方法。当使用特殊硬件和软件的更简单、基于搜索的方法被证明更加有效时，这些基于人类知识的国际象棋研究人员并不是好失败者。他们说，这次“暴力”搜索可能赢了，但这不是通用策略，而且也不是人们下棋的方式。这些研究人员希望基于人类输入的方法能够获胜，但当他们没有做到这一点时感到失望。

A similar pattern of research progress was seen in computer Go, only delayed by a further 20 years. Enormous initial efforts went into avoiding search by taking advantage of human knowledge, or of the special features of the game, but all those efforts proved irrelevant, or worse, once search was applied effectively at scale. Also important was the use of learning by self play to learn a value function (as it was in many other games and even in chess, although learning did not play a big role in the 1997 program that first beat a world champion). Learning by self play, and learning in general, is like search in that it enables massive computation to be brought to bear. Search and learning are the two most important classes of techniques for utilizing massive amounts of computation in AI research. In computer Go, as in computer chess, researchers' initial effort was directed towards utilizing human understanding (so that less search was needed) and only much later was much greater success had by embracing search and learning.

  

计算机围棋领域也出现了类似的研究进展，只是又延迟了 20 年。最初的巨大努力是通过利用人类知识或游戏的特殊功能来避免搜索，但一旦搜索得到大规模有效应用，所有这些努力都被证明是无关紧要的，甚至更糟。同样重要的是利用自我对弈学习来学习价值函数（就像在许多其他游戏甚至国际象棋中一样，尽管学习在 1997 年首次击败世界冠军的程序中并没有发挥重要作用）。通过自我游戏学习，以及一般的学习，就像搜索一样，它可以进行大量计算。搜索和学习是人工智能研究中利用大量计算的最重要的两类技术。在计算机围棋中，就像在计算机国际象棋中一样，研究人员最初的努力是为了利用人类的理解（因此需要更少的搜索），直到很久以后，通过拥抱搜索和学习才取得了更大的成功。

In speech recognition, there was an early competition, sponsored by DARPA, in the 1970s. Entrants included a host of special methods that took advantage of human knowledge---knowledge of words, of phonemes, of the human vocal tract, etc. On the other side were newer methods that were more statistical in nature and did much more computation, based on hidden Markov models (HMMs). Again, the statistical methods won out over the human-knowledge-based methods. This led to a major change in all of natural language processing, gradually over decades, where statistics and computation came to dominate the field. The recent rise of deep learning in speech recognition is the most recent step in this consistent direction. Deep learning methods rely even less on human knowledge, and use even more computation, together with learning on huge training sets, to produce dramatically better speech recognition systems. As in the games, researchers always tried to make systems that worked the way the researchers thought their own minds worked---they tried to put that knowledge in their systems---but it proved ultimately counterproductive, and a colossal waste of researcher's time, when, through Moore's law, massive computation became available and a means was found to put it to good use.

  

在语音识别方面，早在 20 世纪 70 年代就有了一场由 DARPA 赞助的竞赛。参赛者包括许多利用人类知识的特殊方法——单词、音素、人类声道等知识。另一方面是更新的方法，它们本质上更具统计性，并进行更多的计算，基于隐马尔可夫模型（HMM）。统计方法再次战胜了基于人类知识的方法。这导致了整个自然语言处理领域的重大变化，几十年来逐渐发生，统计和计算开始主导该领域。最近语音识别领域深度学习的兴起是朝着这个一致方向迈出的最新一步。深度学习方法对人类知识的依赖更少，并使用更多的计算，再加上在巨大的训练集上学习，可以产生更好的语音识别系统。就像在游戏中一样，研究人员总是试图制造出按照研究人员认为自己的思维方式工作的系统——他们试图将这些知识放入他们的系统中——但事实证明，这最终适得其反，并且极大地浪费了研究人员的时间，当通过摩尔定律，大规模计算变得可用并且找到了充分利用它的方法时。

In computer vision, there has been a similar pattern. Early methods conceived of vision as searching for edges, or generalized cylinders, or in terms of SIFT features. But today all this is discarded. Modern deep-learning neural networks use only the notions of convolution and certain kinds of invariances, and perform much better.

  

在计算机视觉领域，也存在类似的模式。早期的方法将视觉视为搜索边缘、广义圆柱体或 SIFT 特征。但今天这一切都被抛弃了。现代深度学习神经网络仅使用卷积和某些不变性的概念，并且性能更好。

This is a big lesson. As a field, we still have not thoroughly learned it, as we are continuing to make the same kind of mistakes. To see this, and to effectively resist it, we have to understand the appeal of these mistakes. We have to learn the bitter lesson that building in how we think we think does not work in the long run. The bitter lesson is based on the historical observations that 1) AI researchers have often tried to build knowledge into their agents, 2) this always helps in the short term, and is personally satisfying to the researcher, but 3) in the long run it plateaus and even inhibits further progress, and 4) breakthrough progress eventually arrives by an opposing approach based on scaling computation by search and learning. The eventual success is tinged with bitterness, and often incompletely digested, because it is success over a favored, human-centric approach.

  

这是一个很大的教训。作为一个领域，我们还没有彻底了解它，因为我们还在继续犯同样的错误。为了看到这一点并有效地抵制它，我们必须了解这些错误的吸引力。我们必须吸取惨痛的教训，从长远来看，建立我们的思维方式是行不通的。这个惨痛的教训是基于历史观察：1）人工智能研究人员经常试图将知识构建到他们的代理中，2）这在短期内总是有帮助的，并且对研究人员个人来说是令人满意的，但3）从长远来看停滞不前，甚至抑制进一步的进展，4）突破性的进展最终通过基于搜索和学习的缩放计算的相反方法实现。最终的成功带有苦涩的色彩，而且往往无法完全消化，因为它是相对于受青睐的、以人为本的方法的成功。

One thing that should be learned from the bitter lesson is the great power of general purpose methods, of methods that continue to scale with increased computation even as the available computation becomes very great. The two methods that seem to scale arbitrarily in this way are search and learning.

  

应该从惨痛的教训中学到的一件事是通用方法的强大力量，即使可用计算变得非常大，这些方法也可以随着计算的增加而继续扩展。似乎以这种方式任意扩展的两种方法是搜索和学习。

The second general point to be learned from the bitter lesson is that the actual contents of minds are tremendously, irredeemably complex; we should stop trying to find simple ways to think about the contents of minds, such as simple ways to think about space, objects, multiple agents, or symmetries. All these are part of the arbitrary, intrinsically-complex, outside world. They are not what should be built in, as their complexity is endless; instead we should build in only the meta-methods that can find and capture this arbitrary complexity. Essential to these methods is that they can find good approximations, but the search for them should be by our methods, not by us. We want AI agents that can discover like we can, not which contain what we have discovered. Building in our discoveries only makes it harder to see how the discovering process can be done.

  

从这个惨痛的教训中我们要学到的第二个要点是，心灵的实际内容是极其复杂的，无可救药。我们应该停止尝试寻找简单的方法来思考思想的内容，例如思考空间、物体、多重主体或对称性的简单方法。所有这些都是任意的、本质上复杂的外部世界的一部分。它们不应该被内置，因为它们的复杂性是无穷无尽的；相反，我们应该只构建可以找到并捕获这种任意复杂性的元方法。这些方法的本质是它们可以找到好的近似值，但对它们的搜索应该是通过我们的方法，而不是我们自己。我们希望人工智能代理能够像我们一样进行发现，而不是包含我们已经发现的内容。建立我们的发现只会让我们更难了解如何完成发现过程。
