# DNN-assisted statistical analysis of a model of local cortical circuits
[paper](https://www.nature.com/articles/s41598-020-76770-3)

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
大脳皮質のメカニズムを解明するためには，計算機を用いたモデル化が有効である。しかし，適切な解析ツールがないことや，高次元パラメータ空間を体系的に数値解析するには膨大なコストがかかることから，大規模なネットワークモデルの構築や解析，さらには根本的な原理の抽出は，それ自体が困難な課題となっていた。そこで本稿では、ディープニューラルネットワーク（DNN）を用いたデータ駆動型のアプローチを提案する。これは、まず特定の入出力関係を発見し、次にこの情報と、十分に訓練されたDNNの優れた計算速度を利用して、パラメータ探索を導き、理論的な理解を得るというものである。この新しいアプローチを説明するために、大脳皮質の局所回路をモデル化するためのintegrate-and-fireニューロンの中規模ネットワークをテストケースとして使用した。正確かつ非常に効率的なDNNサロゲートの助けを借りて、モデルの応答の統計を明らかにし、モデルの動作の詳細な画像を提供しました。得られた情報は、一般的かつ基礎的なものであり、神経科学に直接応用できるものである。今回提案した手法は、他の生物学的モデリング手法と併用することで、より大規模で複雑な生物学的ネットワークに拡張できることが示唆された。

