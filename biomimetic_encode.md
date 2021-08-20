# A biomimetic neural encoder for spiking neural network
[paper](https://www.nature.com/articles/s41467-021-22332-8)

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


## Intro

しかし、光、音、匂い、温度などの外部刺激や、血圧、酸素濃度、痛みや空腹感などの内部刺激は、主にアナログの時間的な連続変数である。感覚ニューロン（求心性ニューロン）は、特定の種類のアナログ刺激を、1つまたは複数の神経エンコーディングアルゴリズムに従って対応するスパイク列に変換し、その後、スパイクエンコーディングされた情報を中枢神経系に中継して処理する必要があります。

感覚伝達には固有の確率があり、これにより神経細胞はノイズ耐性とエネルギー効率を高めて情報を処理することができる6,7。