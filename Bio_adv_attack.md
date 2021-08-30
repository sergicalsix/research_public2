# Bio-Inspired Adversarial Attack Against Deep Neural Networks
[paper](https://arxiv.org/pdf/2107.02895.pdf)

<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/x-mathjax-config">
 MathJax.Hub.Config({
 tex2jax: {
 inlineMath: [['$', '$'] ],
 displayMath: [ ['$$','$$'], ["\\[","\\]"] ]
 }
 });
</script>
## Abstruct
本論文では、生物にヒントを得たデザインを動く物理的物体に適用することに基づいて、ディープニューラルネットワーク（DNN）に対する新しい敵対的攻撃を開発しています。我々の知る限り、これは動く物体を使った物理的攻撃を導入した最初の作品です。本論文では、デジタル入力や静止した物理的物体に小さな摂動を導入するという、既存の文献で支配的な攻撃戦略に従うのではなく、2つの新しい成功した攻撃戦略を示しています。

1つの物理物体に複数のパターンを重ね合わせることで、DNNは混乱し、クラスラベルを割り当てるためにパターンの1つを選択することを示している。また、3台の羽ばたきロボットを用いた実験では、DNNのミスを誘発するようなカモフラージュを開発できる可能性を示した。また、ある種の動きは、ビデオの連続したフレーム間の依存性を低下させ、物体検出器を「ブラインド」にしてしまうことも示している。したがって、DNNに対する物理的な攻撃を成功させるためには、システムに対する標的となる動きも考慮する必要があります。

