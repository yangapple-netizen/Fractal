分形理论(Fractal Theory)是当今十分风靡和活跃的新理论、新学科。分形的概念是美籍数学家本华·曼德博（法语：Benoit B. Mandelbrot）首先提出的。分形理论的数学基础是分形几何学，即由分形几何衍生出分形信息、分形设计、分形艺术等应用。

具有自相似性的形态广泛存在于自然界中，如：连绵的山川、飘浮的云朵、岩石的断裂口、粒子的布朗运动、树冠、花菜、大脑皮层……Mandelbrot把这些部分与整体以某种方式相似的形体称为分形(fractal)。

根据自相似性的程度，分形可以分为有规分形和无规分形，有规分形是指具体有严格的自相似性，即可以通过简单的数学模型来描述其相似性的分形，比如三分康托集、Koch曲线等；无规分形是指具有统计学意义上的自相似性的分形，比如曲折连绵的海岸线，漂浮的云朵。世间万物都可以分为确定性和随机性两种情况，分形的这两种分类就是确定性和随机性的泛化。


分形几何的概念是美籍法国数学家曼德布罗（B.B.Mandelbrot）1975年首先提出的，但最早的工作可追朔到1875年，德国数学家维尔斯特拉斯（K.Weierestrass）构造了处处连续但处处不可微的函数，集合论创始人康托（G.Cantor，德国数学家）构造了有许多奇异性质的三分康托集。1890年，意大利数学家皮亚诺（G.Peano）构造了填充空间的曲线。1904年，瑞典数学家科赫（H.von Koch）设计出类似雪花和岛屿边缘的一类曲线。1915年，波兰数学家谢尔宾斯基（W.Sierpinski）设计了象地毯和海绵一样的几何图形。这些都是为解决分析与拓朴学中的问题而提出的反例，但它们正是分形几何思想的源泉。1910年，德国数学家豪斯道夫（F.Hausdorff）开始了奇异集合性质与量的研究，提出分数维概念。1928年布利干（G.Bouligand）将闵可夫斯基容度应用于非整数维，由此能将螺线作很好的分类。1932年庞特里亚金（L.S.Pontryagin）等引入盒维数。1934年，贝塞考维奇（A.S.Besicovitch）更深刻地提示了豪斯道夫测度的性质和奇异集的分数维，他在豪斯道夫测度及其几何的研究领域中作出了主要贡献，从而产生了豪斯道夫-贝塞考维奇维数概念。以后，这一领域的研究工作没有引起更多人的注意，先驱们的工作只是作为分析与拓扑学教科书中的反例而流传开来。
真正令大众了解分形是从计算机的普及肇始，而一开始，分形图的计算机绘制也只是停留在二维平面，但这也足以使人们心驰神往。近来，一个分形体爱好者丹尼尔•怀特（英国一钢琴教师）提出一个大胆的方法，创造出令人称奇的3D分形影像，并将它们命名为芒德球（mandelbulb）。

Mandelbrot集和julia集的核心公式都是 f(z) = z^2 + c。区别在于Mandelbrot Set是在z = 0处，对复平面上每一点c进行迭代计算，若每一个 |f(z)| 小于2，则其属于集合内，当然，我们在计算机计算时只能设定一个迭代次数，超过迭代上限仍然模小于2的认为属于集合。Julia Set则是对于设定的一个常数c(其模假定小于2)，对复平面内的每一点z进行迭代计算，若满足模小于2则属于集合。所以Mandelbrot集是julia集的子集。Mandelbrot集和julia集描述的是一个集合，所以称之为“集”，Mandelbrot集合Julia集是在研究集合的过程中发现的。而一些没有参数的分形方法，如康拓三分、科赫、谢尔宾斯基分形描述的都是一个分形图片。

Mandelbrot集只是一个集合，所以只有两种颜色。要想得到更cool的结果还需要采用orbit trap的方法进行着色。每次迭代中， z对应于orbit中的一点，最简单直接的orbit trap就是计算orbit中每个点到某一个固定点（原点？）的平均距离，然后根据距离值到color table中取颜色。也可以采用更复杂的orbit trap来获得更impressive的着色，比如计算orbit到某函数曲线的距离等。

IFS是分形的重要分支。它是分形图像处理中最富生命力而且最具有广阔应用前景的领域之一。这一工作最早可以追溯到Hutchinson于1981年对自相似集的研究。美国科学家M.F.Barnsley于1985年发展了这一分形构型系统，并命名为迭代函数系统（Iterated Function System，IFS），后来又由Stephen Demko等人将其公式化，并引入到图像合成领域中。IFS将待生成的图像看做是由许多与整体相似的（自相似）或经过一定变换与整体相似的（自仿射）小块拼贴而成。

IFS算法：
1.设定一个起始点（x0，y0）及总的迭代步数。
2.以概率P选取仿射变换W，形式为
X1=a x0+b y0 +e
Y1=c x0+d y0+f
3.以W作用点（x0，y0），得到新坐标（x1，y1）。
4.令x0=x1，y0=y1。
5.在屏幕上打出（x0，y0）。
6.重返第2步，进行下一次迭代，直到迭代次数大于总步数为止。

分形必然涉及递归，分形像俄罗斯套娃一样。

世界就是分形的，每一个领域都像一个窗户，进入窗户之后又能看到一个完整的世界。

分形的计算很适合并行，可以用tensorflow来做。

豪斯多夫维


http://www.matrix67.com/blog/archives/292
https://christopherolah.wordpress.com/2011/08/08/the-real-3d-mandelbrot-set/
https://www.zhihu.com/question/20825938/answer/26438732
https://www.douban.com/note/230496472/
