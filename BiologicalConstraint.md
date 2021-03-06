#題名
[paper](https://www.nature.com/articles/s41583-021-00473-5)

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
ここでは、局在型、自己結合型、異種結合型、深層型、全脳型など、さまざまなタイプの神経モデルを取り上げ、生物学的妥当性を向上させるためのポイントを明らかにします。これらの側面は、モデルニューロンの選択、シナプス可塑性と学習のメカニズム、抑制と制御の実装、面的構造や局所的・長距離的な結合性などの神経解剖学的特性など多岐にわたります

## Intro
ニューラルネットワークをより神経的にするために役立つ7つの脳の制約を紹介します（図1）( ニューロンモデルの性質、シナプス可塑性と学習の実装、興奮性ニューロンと抑制性ニューロンの相互作用による調節と制御、総体的な解剖学的構造と領域の細分化、領域内の局所的な接続性と領域間の大規模な接続性 )

確立されたタイプの認知ニューラルモデル（図2）と、いくつかの脳の制約を新しい方法で統合したニューラルシミュレーションの例を紹介します。


### 自己組織化ネットワーク
神経解剖学的観察によると、大脳皮質はニューロン間の十分な内在的かつ反復的な接続性を特徴としており、したがって、連想記憶と見なすことができます19,20。このような観点から、「自己連想ネットワーク」または「アトラクタ・ネットワーク」と呼ばれる人工的なニューラルネットワークの一群が生まれました21,22,23,24,25,26,27,28,29,30,31,32

オートアソシアティブ・ネットワーク・モデルは、ニューロンのメンバー間に接続を持つニューロンを実装しているため、各ニューロンはセットに含まれる他のニューロンのいくつか、あるいはすべてと相互にリンクします。これは、後述する異種結合ネットワークとは対照的で、各ニューロンプール内での接続はなく、ネットワークニューロンのサブ集団間で接続が実行されます。

自己組織化ネットワークにおける学習の効果をシミュレートするために、ニューロンの事前の活動の結果としてニューロン間の接続重みを変化させる、いわゆる学習ルールが含まれています。例えば、生物学的に確立された教師なしのヘブ型学習は、共同で活性化されたニューロン間の接続を強化するもので5、頻繁に適用され、弱い接続の自己結合ニューロンプール内に強い接続のセルアセンブリが形成されます（図2b）。これらの細胞集合体は、分散型ネットワークの相関関係や、知覚、認知、あるいは「混合」された文脈依存の知覚-認知状態の表現として機能します6,30,32,33,34。したがって、皮質ニューロンがグループで協力して働くことや、表現がそのようなグループに分散しているという観察結果14,18は、学習メカニズムとともに、この人工的なネットワークタイプに対応することができ、ローカリズムネットワークの主要な欠点を克服することができます

これは、ゲシュタルト補完のメカニズムとして考えられている。つまり、部分的な入力（尻尾と前足）だけで物体（猫など）を認識することができる。このメカニズムは、図2bに示されているように、ニューロンαとβを刺激するだけで、ニューロンα、β、γで形成される細胞集合体が活性化される。 
さらに、オートアソシアティブ・ネットワークは、皮質の神経コードが疎である（つまり、ある（複雑な）刺激に対して、利用可能なニューロンのごく一部しか反応しない）15,18,22,35,36という観察結果と、いくつかの（他の）ニューロンが、いくつかの刺激のうち、初歩的で頻繁に発生する特徴に反応する（したがって、あまり疎ではない方法で行動する）37という観察結果を統合したものである。この理由は、細胞集合体の重複にあります。つまり、2つ以上のこのような回路が、機能的には別々でありながら、ニューロンを共有できる可能性があるということです。図2bでは、ニューロンα、β、γとニューロンγ、δ、εで形成される細胞集合体の「オーバーラップニューロンγ」がこれを示している。

## ヘテロアソシアティブネットワーク
ヘテロアソシアティブネットワークは、2つ以上のニューロンプールまたは「層」を含み、層内ではなく層間で接続されます51,52。これらのモデルは、異なるニューロンプールを順番に接続して構成されています。この接続方式は、神経生物学的な構造（例えば、網膜の層間や皮質領域間の次隣接フィードフォワード接続）にヒントを得ています53。

並列分散処理で頻繁に使用される「多層パーセプトロン」と呼ばれるモデルのクラスは、3つのニューロン層を含み、1つの層が入力を受け取り、1つの層が出力を生成し、その間に1つの「隠れ」層がある52（図2c）。このようなネットワークでは、認知的実体の表現が高密度かつ非疎なものとなります。つまり、隠れ層のすべてのニューロンに分散しており、層全体の活性化ベクトルが、物体、単語、意味、思考のネットワーク上の相関関係となるのです54。これらの表現は、密度が高く、「完全に分散している」という性質を持っており、多くの自己連想ネットワークを特徴づける疎な（しかし、分散している）表現とは対照的である。

このようなネットワークでは、入力と出力の「教師」信号をそれぞれ入力層と出力層に与え、シナプスの重みを調整することで、入力と教師出力の関係を学習させる。シナプスの重みを調整するために、教師付き学習アルゴリズムが適用される。このアルゴリズムは、出力層から問題のシナプスに向かって逆方向に計算される誤差勾配に従って重みを調整する。当初は「誤差逆伝播」と呼ばれるアルゴリズムが適用されていたが55、最近ではネットワーク全体の誤差勾配に基づいた様々な学習ルールが利用できるようになり、「勾配依存」学習の様々なバリエーションが可能となっている56。

記憶プロセスを実装するために、3層構造にさらに1つの層を追加し、「隠れ」層と相互に接続した57。この「単純再帰ネットワーク」構造は、残響的な活動を引き起こす。自動連想ネットワークと同様に、3層または4層のフィードフォワードネットワークは、幅広い認知機能の実現に成功している58,59,60。


## Deep 
層数を3層から6層以上に増やす神経生物学的な動機は、物体処理のための後頭側頭葉腹側流の神経解剖学的構造にあります。この神経解剖学的構造では、一次視覚野（V1）から隣接する領域、そして複数のレベルを経由して前頭側頭領域へと神経接続がつながっています65。

DNNはいくつかの重要な点で変化している。例えば、畳み込みDNNでは、隣接する入力の共同処理を容易にするために、層間（一部の層）に位相差投影が行われ、リカレントDNNでは、時間をかけて情報を維持することを可能にするために、層間の相互接続や層内のリカレントリンクが行われる。これらの改良により、物体分類66,67や音声認識68,69,70をはじめとするいくつかの認知領域において、人間に近い性能レベルに達した非常に強力なデバイスが生み出されている。DNNは、複雑なデータセットに直接フィットするオーバーパラメータ化されたブラインドプロセスを内在する正則化で実行し、局所的な補間に基づく汎化を可能にすることで、これまで離散的なルールに帰属していた機能を担うことが提案されている71。


大規模な成功を収めたDNNだが、最近ではその限界が指摘されている。例えば、人間には全く認識できないような画像を、特定の物体のインスタンスとして高い信頼度で分類するなど、DNNは不適切な汎化行動を示すことがある72,73,74,75。同様に、いわゆる敵対的な例に関する広範な研究により、画像へのわずかな摂動が、人間には感知できないにもかかわらず、DNNによる重大な誤分類を引き起こすことが示されている72,76。


## 全脳型ネットワーク
ニューラルネットワークの各層間の接続は、一般的には隣り合う領域がつながっているだけの単純なものだが、多数の領域が複雑につながっている大脳皮質の接続構造とは異なっている。脳を領域と核に複雑に分割し、これらの構成要素間の神経解剖学的な接続性を近似的に実装することは、「全脳」モデリングの主な目的です。ほとんどの「全脳」モデルは、脳のすべての部分をモデル化するのではなく、皮質と前脳の核、またはその一部に焦点を当てています。


## 脳の制約

### 異なるレベルでの統合
これまでのモデリングでは、単一のニューロン104,105、皮質の局所回路106,107,108,109におけるニューロンの相互作用、または皮質領域間のグローバルな相互作用（「全脳ネットワーク」の項を参照）のレベルでニューロン機能を近似することを目的として、特定の粒度に焦点を当てていました。脳の構造と機能の異なるレベルで同時に制約を適用するためには、これらの異なるレベルに対応し、1つのモデルに統合する必要があります。さらに、モデルの検証に複数の実験データを利用するためには、マルチレベルモデリングが必要です101,110,111,112。


### ニューロンのモデル
このモデルは、単一のニューロンの発火確率や、局所的なニューロン回路の累積活動をシミュレートするものと解釈できます。より洗練されたスパイク型の「統合・発火」ニューロンは、シナプス後電位の合計とその結果としてのニューロンの発火をモデル化しており、樹状突起のコンパートメントや入力間の非線形相互作用を統合するように拡張することができる104,122,123,124,125。マルチコンパートメントモデルや生物物理学的ニューロンモデルでは、樹状突起ツリーの細分化、シナプス後のイオンチャネルダイナミクス、樹状突起活動電位など、さらに詳細な情報を含めることができます

さらに、ニューロンの活動の中には、入力によって説明することが困難なものがあり、それはノイズと見なすことができます130。このように、ノイズを加えることと、順応（活性化が長く続くと活動が低下すること）により、ニューロンモデルのリアリズムの度合いをさらに高めることができます。

一方で、高度なニューロンモデルは、必要な計算資源が多いため、認知に関連する領域内および領域間の相互作用の大規模シミュレーションには適用できないのが現状である。


### シナプス可塑性と学習
脳内の複数の学習システムをモデル化するためには、教師あり、教師なしの両方の主要な学習形態を実装する必要があります。

fire together-wire together」の原理を実装すると、共同で活動するニューロン間の接続の長期増強（LTP）につながります。また、より神経生理学的に詳細なルールもあり、特に、LTPと、無相関または反相関の活性化の結果としての長期抑圧（LTD）の両方を実現できるものがある132,133。

教師付き学習では、パフォーマンスが適切であったか、間違っていたか、誤りであったかを個人やネットワークに知らせるフィードバック信号を使用する。しかし、教師付き学習のシミュレーションで使用されるアルゴリズムの選択は、生物学的な妥当性だけでなく7,138、勾配依存学習の計算上の有効性が大きな役割を果たしている55,56,62。これらの後者のアルゴリズムが生物学的に現実的であり、特定の認知領域における高度な学習に適用できるかどうかは議論の余地があります。研究者の中には、誤差勾配を計算してフィードフォワードニューロンネットワークを介してフィードバックするメカニズムには強力な生物学的裏付けがないと批判する者もいるが、一方で、そのような側面を部分的にサポートしうる神経生物学的メカニズムの証拠が最近出てきたと指摘する者もいる


### 抑制と制御
より現実的なニューラルネットワークモデルでは、興奮性ニューロンと抑制性ニューロンの要素が含まれており、覚醒や注意に不可欠なメカニズムであるこれらのニューロンの相互作用によって活動の調節と制御が行われている（「最近の進展と傾向」のセクションを参照）。局所的な調節機構とグローバルな調節機構の両方を実現しているモデルは少ない

###  領域レベルでの構造

### 領域内の局所結合性
大脳皮質の最も一般的な興奮性ニューロンである錐体細胞は、それぞれ10,000〜40,000本の樹状突起20,156を持ち、それぞれの樹状突起には通常1つのシナプス20が含まれています。したがって、大脳皮質の150億から320億個のニューロンの中で、これらの細胞の1つが、数万個の他の皮質細胞と接触する可能性がある157。その数は1014個以上と膨大なため、遺伝情報だけでは判断できず、特定の神経細胞のペアが接続されているかどうかは、確率的な原理で決定される。隣接する2つの錐体細胞が接続される確率は、その距離が長くなるほど低下する20,101,158,159。神経解剖学的研究によると、大脳皮質領域内の局所的な興奮性接続は疎であり、隣接するニューロン間のリンクに近隣バイアスがかかっていることが示されている20,160。

これらの特徴を考慮すると、異種結合ネットワークの層内接続の欠如は、生物学的に現実的ではないと思われる。自己結合層や領域21,22,28,161を含むネットワークの多くは、これらの領域内のすべてのニューロン間の完全な結合を含んでおり、同様に、単純再帰ネットワーク57の記憶層はすべての再帰結合を持っています。このような完全な自己結合性は、大脳皮質に内在する局所的な結合の疎さとは対照的です。脳の制約である、疎で局所的で部分的にランダムな接続と近隣バイアスは、自己結合性と領域間の異種結合性を結びつける神経回路網で実現されています24,149,150,162。局所的な接続性の制約に関して最も進んでいるのは、新皮質の各層における異なる細胞タイプとその位置を実現する微小回路モデルである109,110,152,154,163。しかし、現在利用可能なほとんどのニューラルネットワークでは、領域内接続性制約の実装が生物学的リアリズムの向上につながっています101。


### 領域間のグローバルな結合
大脳皮質の領域間の接続は、いくつかの一般的なルールに従っています。ほとんどのリンクは相互につながっています。隣接する領域はほとんどの場合相互にリンクしており、2番目に近い隣人は多くの場合接続されています20,164。しかし、より長い距離のリンクは疎であり、侵襲的技術（例えばトレーサーを用いたもの）や非侵襲的技術（拡散テンソル画像や拡散強調画像など）を用いて正確にマッピングするために多くの努力が払われてきた


## 最近の研究

 マカクの視覚系の32の皮質領域における神経生理学的活動をモデル化した154。
 
### 認知理論を脳に結びつける
特に、表現上の類似性分析により、下側頭皮質の神経代謝活動が、視覚的に知覚された物体の意味上の類似性を反映していることが明らかになりました186。

最近の研究では、DNNにリカレント接続を含めることが、側頭皮質で観察される高速の神経生理学的ダイナミクスの側面を捉えるために重要であることが示されている188。

### 言語処理と推論
認知脳機能を神経生物学的な形式でモデル化する比較的簡単な方法は、一連の領域と核を選択し、それぞれを一連のニューロンを用いてモデル化し、認知機能をモデル領域に割り当て、領域固有の活性化ベクトル間の事前定義または学習されたマッピングを用いてそれらの間の相互作用を決定することである。この戦略により、概念、言語、数の処理などの認知機能の生物学的なモデルが生まれた

### 記憶
活性化閾値とシナプス重みを適切に調整すれば、完全に接続された自己連想記憶は持続的なアトラクタ状態を特徴とし、ワーキングメモリとの相関関係が考えられる22,201,202。スパイキングニューロンを用いたモデルでは、その「領域」内ですべての接続性を持つ自己結合ネットワークは、ワーキングメモリの実験中に下側頭葉のニューロンから記録されたものと同様の発火パターンを生じさせた39,46,203。

### 概念
このようなマルチモーダルな情報の統合には、（互いに離れた）異なる皮質領域にあるモーダル特有の神経システム間を橋渡しする接続が必要であり、概念処理における大規模な接続構造の役割を示唆している。


現実的な初期言語学習シナリオ、教師なし学習、解剖学的に制約された局所的および全体的な結合性を適用して、前頭葉と側頭葉の皮質における単語学習プロセスをモデル化したところ、概念処理と意味処理のための神経回路の分布がデータと一致した。具体的には、符号とそれに関連する物体や行動に関する情報を共同処理した結果として形成された概念回路（図5）のほとんどのニューロンは、モデルのマルチモーダルコンバージェンスハブに収容されており、感覚運動情報が大脳皮質に到達する領域から最も強く接続されたコネクターハブ領域に向かって全体的に「引っ張られる」ことを説明している。
 