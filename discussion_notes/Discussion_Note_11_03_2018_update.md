Unifying account of visual motion and position perception
Oh-Sang Kwona,1, Duje Tadina,b,2, and David C. Knill

ZRY: 我是这篇paper一个被试。之前做了很多年但是没有大的理论突破。
YFT：非常同意
ZRY：Harvard vision lab这几年一直基于现象学，这篇文章是一个非常大的突破。用kalman filter解释这个现象。
YFT：surprisingly basic, 竟然没人做过。

YFT：心理学出身的人做不到这个level，想不到像这样一个简单的模型解释的这么好。AY说，跟心理学人聊tracking, surprisingly none of them know what kalman filter is.心理学人研究这么多年，没人用过kalman filter。

ZRY：最难点的是把两方面的知识同时装到同一个人的脑子里。

ZM：往做CV的人脑子里装心理学知识要比反过来容易很多

ZRY： OSK作者之一上学的时候学的是很engineer的东西。写code真的很难。

YFT：写kalman fitler可能很容易，但是怎么fit model?

ZRY: 算data的likelihood。问题难道有这个idea和背景，能把paper做出来。

YHJ：是不是应该学习跟Face有关的机器学习的东西。
ZM：应该，现在是大趋势。

MA：最喜欢实验三，根据理论Predict一个现象，很聪明。之前的实验都是我可以解释这个，解释那个。
ZRY：像元素周期表一样，找到理论，还可以Predict新的存在

YFT：以来发现新的现象，而来把vector sum模型好好搞一搞。这个模型已经很多年了，当年是nature neurosicence

ZRY：是很intuitive的解释。2001paper中的vector sum和这里提到的不是一回事，那里说的是两个pattern motion的相加，这个不是，这个是object motion 和pattern motion相加。

YFT：还有一篇也是说Object motion 和pattern motion相加的

YFT: 不fair，vector sum 模型没有eccentricity dependent factor。但是其实就算vector sum模型加了，也很奇怪，因为本身就没有。

ZRY：第三个实验根本没有fitting。实验一中fit出来的parameter可以完全预测实验三行为，我完全不记得有别的模型可以做到这一点。

YFT：这确实是这个模型很厉害的一点，非常同意，结果非常漂亮。

MZ：我觉得我可以退出学术界了，他们把我想做的都做很好了。

ZRY：但是依然被NN拒了，都没有审稿直接拒了

YFT：问题太小？

ZRY：但是别的NN paper不一定好啊

YFT：题目起的不好，scope太小。只focus motion position。应该是Motion只是用来研究一个大问题的工具

ZM：那你起什么title?我们想让一个稍微有一点科学背景的人看到title就很想看这篇paper，觉得很重要。

ZRY：Optimal integration of world model and sensory statistics in dynamic vision

YFT：significance 最后一句话：
a unifying framework that reconceptualizes how the human visual system constructs coherent percepts from noisy position and motion signals.
ZRY：bayesian在perception的应用，都没有涉及到动态的问题。在动态环境中还是在做bayesian inference。intro可以说：在静态下bayesian得到证明，那么动态环境下呢？

ZRY：Optimal integration of world and observer model in dynamic vision

YFT：这个title可能实验要大改，目前实验不能说明这个问题

YHJ：Unifying account of dynamic vision？
MZ：会不会太宽泛。

MZ：更喜欢internal model这个词。

ZRY：internal model = world model，这个模型不一定是对的
Optimal integration of internal model and sensory statistics in dynamic vision

David Knill 写东西比较保守，所以牛逼没有吹很大，没有这么写。


ZRY：给slow speed prior 提了一种全新的解释。你完全可以没有slow speed prior存在，而解释为什么改变contract知觉到的速度不同。

YFT：peripheral noise太大导致的吗？

ZRY: pattern motion 被算成了object motion

YFT：那如果没有pattern motion呢，没有Low speed prior 了吗？我理解的slow speed prior是广泛存在于各种运动中的。

ZRY：contrast降低觉得动的更慢，普遍解释是有一个slow speed prior。而这篇文章不需要这个prior就能解释。
MZ：YFT的意思是这个模型可能没办法解释一个没有pattern motion，只有translation motion的情况下的slow speed prior.

ZRY:我的意思是至少从这个实验来说，对pattern motion的解释是很好的。站在我的角度这个点是最牛的。而OSK说他并不想over sell这个点，想主要卖kalman filter.

YFT:如果要卖slow speed prior需要重新做实验。增加eccentricity 只是side product，主要还是解释Motion induced position shift。最好的卖点还是Unifying account。如果要卖slow speed还是要重新做一套专门的slow speed实验。

ZRY： YFT你认为slow speed prior是存在的，我们在找解释。而我认为这只是一个现象的解释，并不一定存在，可能别的来解释。

YFT：另一个解释。Chris Sims的那篇文章，我用information theory解释很多现象，之前是被Shepard用exponential principle来解释，Chris Sims 提出了一个mechanism的解释，同时还可以说你之前之所以提出你的理论，只是因为你观察到了我这个mechanism的结果。同样的，本篇文章提供的也是一个更mechanism的解释，也许slow speed prior只是一个by product

ZRY：slow speed prior可能不是一个现象，只是模型中加一个component可以解释结果。可能不存在。

ZRY：bias是存在的，但是prior的概念只存在于bayesian理论中，你可以用bayesian理论解释很多现象，很少，但是也有很多现象可以用别的理论解释。Alan Stocker自己可能都在反对slow speed prior. 如果人真的有这个prior，他应该会觉得更快。他的解释是我们还不清楚人的自己的prior真正是什么。

YHJ：类似循环论证，很多现象是ill-defined。人的行为很复杂，我们观察到的东西不一定是全部。

ZRY：你能观察到的就是各种行为，bayesian可以解释很多现象，但是也有很多不能用或者可以用别的解释。

YFT：贝叶斯的prior太ad hoc。我也很不爽，但是我觉得作为experimentalist，我们能做的就是有没有实验能支持这种prior。我觉得无可厚非。我们可以解释为什么这个prior这么来，或者有没有别的可以替代。

ZRY：比如硬件上如何表征prior?

YFT：其实我宁愿用别的模型来解释Prior，比如这个kalman filter

ZRY:我根本上不同意，你认为prior是更高级的，而我认为是平行的。

YFT：对我来说我能接受的是prior被explained out，而在此之前我还是接受。

ZM：nativism v.s. empiricism

ZRY: 第三个实验MZ做eye tracking. saccade看落点在哪。是vector sum,还是领先phase？做5度可能还好。

YHJ：SC对于猴子肯定比对于人重要。

YHJ：为什么FIG2c里面在peripheral不加大size

YFT：可能控制的是retina imaging size.

ZRY: 目的就是为了在外周uncertainty变大。

YFT：外周size变大能否让uncertainty变小。

ZRY：变大之后其实不一定uncertain变小，可能有一个复杂的关系。

MZ：比如变大了离fixaiton近的变好，离得远的变差。所以比较复杂，避免调入黑洞

ZRY：没有控制变化contrast

YHJ：很难manipulate吧

ZRY：不变eccentricity,只变contrast. contrast也有问题，envelope是两个很重要的东西，contrast也会改变envelope，所以不好弄contrast。

ZRY：改变speed uncertainty,但不改变position uncertainty。




