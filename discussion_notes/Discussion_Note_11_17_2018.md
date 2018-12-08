Comparing continual task learning in minds and machines
Timo Flescha,1, Jan Balaguera,b, Ronald Dekkera, Hamed Nilia, and Christopher Summerfield
PNAS 2018

YFT: 没有那么兴奋，就是transfer learning
MZ:但是能想到embedding就很厉害

YFT：一步一步讲实验。人类可以通过block training达到成绩很好，机器不行。首先研究人类block training学到了什么，然后研究机器为什么不行

MZ：不仅是研究人类学到什么，而且研究人类为什么会学成这样，是因为有prior


YFT &YHJ：觉得人类Prior的解释实验做的不好。

YFT:解释图一。其实是一个reinforcement learning, trial and error的实验。通过implicit reward来学习rule。D E 刺激如何认为分类

YHJ：diagnal rule, D的部分奖励的期望可能跟E不等价。

YFT：等价，一样的，这个非常SB的rule，这个space本身由leaf和branch定义的，但是在E里是强行定义一个rule。不管是D还是E 都是线性的，所以你理应都能学到这个boundary。只是说D图的边界比较直观，但是E图不直观。

MZ：我的问题是他说E是nonverbalizable的，但是两个一起说就好啦。

YHJ：同意

YFT：如果我们预先知道如何定义的其实是可以说出来的。但是point在于这个decision rule更难学。

YHJ：但是psychophysics被试都很聪明啊。

YFT：这个实验不一定真的能学会。到底要train多久？Block2和random比很有意思，长很像但是少了randomization。
task average B2最差。

MZ：B2最差结果很有意思。为什么B2最差？

YHJ：会不会有人无视background change?

YFT:应该不会，最后80%正确率

YHJ：最后平台期了。为什么400个trial？不多也不少，但是我希望能看到一些更大数目的结果

YFT:我觉得他可能不太介意，因为他把所有的都画出来了。

YFT：task switch cost？

YHJ：可能random条件switch 比B2少，应该可以补这个分析。

YFT：2B图，不太知道要说什么。

ZRY：task switch是什么意思

YHZ：在test中，同一个颜色连续两个就是task stay,换颜色是task switch

YFT: 把test trial分为两类。

MZ：他想说的是在task switch情况下，block 竟然也有优势，而这本来是Interleave的优势。

YHJ：图C的psychometric很有想法。实线是task-relevant rule,得到的是标准的psychometric, 虚线是irrelevant,如果是完全不想关应该是完全平的。

YFT：我被试做deicision到底多少依靠relevant和irrelevant。

MZ： B2和Int条件更受irrelevant影响。

YHJ：对这两种rule的划分是否足够清晰。B20是最平的最开的。

MZ：D最后就是做了个correlation。两个matrix。一个是模型假设的，一个是实际测得的。

YHJ：另一种方法，区分两种模型。也许可以解释B2为什么最差，因为他可能用的是同一套rule。

ZRY：是用同一种rule，还是说两个情景都用两个维度

YFT：都用ax1 + bx2，但是a和b可能不一样。

ZRY：但是看图D的解释，他说是same linear boundary，所以可能a和b就是一样的？如果真的是这样，这个model很奇怪

YFT：很重要，你倒是学会用一个var，还是两个维度分类。

ZRY：用一个维度还是两个维度，以及我是否学会了cue，我是有两个task还是一个task

YFT:他的linear model不好，应该是两个task a和b不一样。

ZRY：这个linear model很奇怪，应该和a与b也不一样的模型比。

YFT：图3，旋转的rule，本身boundary是two factor boundary。其实要学的就是ax1+bx2，不管是b200还是int都差不多。C这里比较复杂是因为刺激的space和rule的space是不一样的。

MZ：3D linear model尤其不公平，因为选横着选竖着都可以，不明白为什么选竖的

YHJ：rationale是想引出实验二对于Prior的讨论。

YFT：讨论里说做diagonal rule的原因，B200的优势在diagonal rule就没了。

YHJ：可能是Reviewer的建议？

YFT：讨论里说：rule based还是information integration（凭感觉，说不出为什么做出这个判断，而只是stimulus reward association）。实验二是想说block learning是不是通过rule-based strategy来的。

MZ：旋转以后B200没有优势。说明什么？

ZRY：所以旋转45度不是rule-based。说明了block learning的优势只存在于rule-based的learning里？

YFT：让被试在实验前后给对于这个space的arrangement。来测量prior space organization。

ZRY：如果我是个被试我一看就觉得应该按两个维度分，更容易体现block learning的effect。他们只发现了high prior比low prior在B200高，但是我们不是应该更关注Interaction？就是high prior 比 low prior应该block learning - interleaved learning差要大。

YHJ：如何划分high还是low？有可能其实差不多。5a,b和5c d的high和Low不是等价的因为用的是kendall tau。high low 组间的difference是不一样的。

YFT：关于diagonal prior，虽然我们觉得不make sense,但是有可能视觉系统就是这么organize的。

MZ：图4根diagnonal rule prior算，如果是high prior，应该是分成四个三角

YFT：CNN。第一个实验，暴力直接train,输入就是直接的图，然后发现机器B200条件,test时第一个任务成绩特别差。相当于完全忘记了以前看过的。但是如果是Interleave training,就一直很好
有没有办法是CNN也benefit from block training
现在加一个autoencoder的train, 前面1234CNN变小，后面再4321变大，让他unsupervised学这个刺激的latent space，给机器一个prior，再在这个基础上学deicision rule，对于任务一，prior高于No prior，但是始终没有高于Interleaved学习。相当于prior减少了任务一的损失。

MZ：结果说明人应该抛弃所有的prior，都用interleaved training就能100%？

YFT：Discussion里面说。interested in the representation of neural networks.他们想说的是我们不能Interleaved train neuralnetwork，比如学游戏，都是一个任务一个任务学。但是当前CNN都是Interleaved train。这个研究探索的是加prior和embedding是否可以帮助别的任务的block training.

ZRY:真正学习的过程中，很多东西不是预先设定的，你不能预先设定所有任务，所以，学了10个游戏，但是突然来了第11个游戏，应该怎么办？所以还是需要block training。

MZ：能不能学到D的时候，再时不时复习一下ABC？

ZRY:人远比现在的机器做的好，人不会忘。

YHJ：哪怕两套游戏按键不一样，但是人还是会按键。机器可能已经完全不会按了。量的区别和质的区别

ZRY：narrow down一个很简单的reenforcement learning的问题上，人和机器差这么多。

MZ：设计机器人的时候要不要借鉴人

YFT：机器人需要做到人能做到的。AI general ambition是一个nn做所有事情。你可以说人的大脑是不同区的，但是AI的目的是一个neural network能自然形成分区

YHJ：会不会nn太小了？

YFT：最好的也是train了后面忘前面。

ZRY：我想说的是，现在从research的角度讲，psychology task比较人和CNN。涉及到CNN到底要多复杂。正常实验条件下Image都是非常有限的。CNN 一般需要很多。如何解决gap

YFT:如何Properly compare?现在只能qualitatively比较，不能quantitative，人和CNN是否有这个性质，不能数量上直接比较，因为CNN有太多parameter可调。

MZ：用image net pretrained模型，freeze低层 weight，用data augmentation

ZRY:我个人也比较喜欢这篇文章。目前人和CNN 比较两个思路，一种是Neuron活动和CNN的直接比较。第二种思路更有意思一点，train一个nn，里面有些神经元在没有任何生理限制下刚好show出和人的一样。这篇文章是第三种思路，难度更大，怎么去改结构让他更像人，replicate human behavior。做unsupervised learning，提取representation。需要两个背景兼具的人才能做出这种paper。想做好很难。

YFT：难在哪里？

ZRY：最后一步。用autoencoder做出来再train达到不遗忘，很厉害。

YFT：第一、二种思路相似。

YHJ：计算机的实验是不是trial太少了？

YFT：train了40000个image

YFT：为什么要做Prior的实验三，这就跟这个问题有关

YFT:我觉得两个点很有意思。第一，learning和memory的差别，有learning但是没有Memory。现在新的deep reinforcement learning加入了memory component可以做很好，如果这样，是不是在CNN上加memory，能replay，也可以达到加prior的效果。或者加入attention？第二，representation。你对于一个data set的representation到底是什么？pixel的并不能达到很好的效果，但是比如在embedding上represent就可能更好。所有DNN 还是要解决representation是什么的问题。在文章里DNN和autoencoder的结构是一模一样的，区别就是Unsupervised train还是用label train.将来要改CNN不一定是改结构，而是怎么样找到新的正确的representation。

ZRY：两个问题。如果我一开始指导学生加memory呢？

