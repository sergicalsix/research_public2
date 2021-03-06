# Neuroscience-Inspired Artificial Intelligence
[paper](https://www.sciencedirect.com/science/article/pii/S0896627317305093?via%3Dihub#bib2)

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
脳科学と人工知能（AI）の分野には、長い歴史があります。しかし、最近では、この2つの分野間のコミュニケーションやコラボレーションは、あまり一般的ではなくなってきています。本稿では、生物の脳をよりよく理解することが、知的な機械を作る上で重要な役割を果たすと主張します。本稿では、AIと神経科学分野の歴史的な交流を概観し、人間や他の動物の神経計算の研究に触発された現在のAIの進歩を紹介する。最後に、両分野の今後の研究を進める上で鍵となりそうな共通のテーマを取り上げて締めくくります。

## Main text
人間レベルの一般的なAI（または「チューリングパワフル」インテリジェントシステム;チューリング、1936年）の構築は困難な作業であるという前提から始めます。これは、可能なソリューションの検索スペースが広大で、人口が非常に少ない可能性があるためです。



脳が利用するアルゴリズム、アーキテクチャ、機能、表現です。


4つの神経科学的に触発された具体例: 

- Attension 

視覚的注意は場所とオブジェクト間で戦略的にシフトし、処理リソースと表現座標を一連の領域に順番に集中させます

計算コスト（ネットワークパラメータの数など）を入力画像のサイズに合わせて適切にスケーリングすることができました。このアプローチの拡張は、その後、困難なマルチオブジェクト認識タスクで印象的なパフォーマンスを生み出し、精度と計算効率の両方の点で、画像全体を処理する従来のCNNよりも優れている

- Episodic Memory (エピソード記憶)

その知的な行動が複数の記憶システムに依存しているということです

エピソード記憶は海馬

記憶を再生することは複数記憶に密接に関わっている。

海馬　新皮質に統合

- Working Memory

リカレントニューラルネットワーク
LSTM
DNC
 例えば、ディファレンシャル・ニューラル・コンピュータ（DNC）では、ニューラル・ネットワーク・コントローラが外部のメモリ・マトリクスにアタッチして読み書きを行います（Graves et al. この外部化により、ネットワークコントローラは、地下鉄の地図のようなグラフ状の構造を通る最短経路を見つけたり、ハノイの塔タスクの変形でブロックを操作したりするなど、現在LSTMが苦手とする広範囲の複雑な記憶・推論タスクをゼロから（すなわちエンドツーエンドの最適化を介して）学習することができます（図1C）。


- Continual Learning 

弾性」重み連結（EWC）という形で実装されています（Kirkpatrickら、2017年）。EWCは、以前のタスクで重要であると識別されたネットワーク重みのサブセットの学習を減速させることで、これらのパラメータを以前に発見された解に固定するという作用を持ちます（図1D）。

## Future
しかし、機械レベルの知能と人間レベルの知能の間のギャップを埋めるためには、まだ多くの課題があります。このギャップを埋めるためには、神経科学の考え方がますます必要になると考えています。神経科学の分野では、脳イメージングや遺伝子工学などの新しいツールの登場により、神経回路で行われている計算の詳細な特徴が明らかになりつつあり、哺乳類の脳機能の理解に革命が起こることが期待されています（Deisseroth and Schnitzer, 2013）。AIの研究課題のロードマップとして、また計算ツールの供給源としての神経科学の関連性は、以下の主要分野で特に顕著です。


## 物理的世界の直観的な理解
AIの研究では、この課題に対処するための方法が模索され始めている。例えば、シーンを個々のオブジェクトとその関係に分解することで、人間らしい方法でシーンを解釈し、推論する新しいニューラルネットワークアーキテクチャが開発されています

## 効率的な学習
人間の認知能力は、わずかな例から新しい概念について迅速に学習し、事前の知識を活用して柔軟な帰納的推論を可能にするという点で際立っている。この人間の能力をAIの課題として浮き彫りにするために、Lakeらは最近、「Characters challenge」という問題を提起しました（Lake et al.2016）。この課題では、観察者は、見慣れない手書き文字の新しいインスタンスを、たった1つの模範例を見ただけで、他の類似したアイテムと区別しなければならない。人間はこのタスクをうまくこなすことができますが、古典的なAIシステムにとっては難しいタスクです。


1つの例示概念から新しいサンプルを生成することができます

さらに、最近のAI研究では、ワンショットコンセプト学習（Santoro et al., 2016, Vinyals et al., 2016）やRLタスクでの学習の加速をサポートするために、関連する問題での事前の経験を活用して新しいタスクに関する知識を獲得する「学習することを学ぶ」ネットワークが開発されています

## 転移学習

哺乳類の内嗅覚皮質では、細胞は、局所空間を六角形のパターンでタイル状に並べる受容野を持つ、周期的な「グリッド」コードを用いて、同心円状の空間の幾何学性を符号化する

##

バックプロパゲーションの生物学的妥当性に対する第2の核となる反論は、多層ネットワークにおける重みの更新には、非局所的な情報（すなわち、何層も下流のユニットによって生成されたエラー信号）へのアクセスが必要であるというものである（レビューは、Bengio et al. 一方、生物学的なシナプスにおける可塑性は、主に局所的な情報（すなわち、シナプス前後の神経細胞の活動）


近の研究では、階層的な自動エンコーダーネットワークやエネルギーベースのネットワーク（例えば、連続ホップフィールドネットワーク）（Scellier and Bengio, 2016, Whittington and Bogacz, 2017）、つまり予測コーディングに関する理論的な神経科学の考えと強いつながりを持つモデル（Bastos et al. 実際、このようなネットワークでの学習と、スパイクタイミング依存の可塑性（Scellier and Bengio, 2016）、脳全体で広くインスタンス化されているヘブのメカニズム（Bi and Poo, 1998）との間には、具体的な関連性が描かれている。また、異なるクラスの局所学習規則により、階層的な教師付きネットワークが、顔などの物理的に対称な刺激に対する鏡面対称なチューニングなど、生物システムに特徴的な高レベルの不変性を生成できることが示されている