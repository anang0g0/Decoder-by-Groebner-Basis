# Encoding and Decording QC-LDPC

参考文献

１．符号理論　萩原学　2012　日本評論社

２．Error Correcting Coding and Security for Data Networks WILEY Kabatiansky et.al 2005 

３．https://www.researchgate.net/publication/260867979_QC-LDPC_Code-Based_Cryptography

# 20201124

もう一つの符号に挑戦することを思い立った。

https://www.researchgate.net/publication/260867979_QC-LDPC_Code-Based_Cryptography

多分ここでのメインコンテンツはLDPCの復号になると思う。
技術者の中でもこれを実装レベルで理解している人ってどのくらいいるんだろう？


# 20201123

OTその1をQC-LDPCで復活させる。（調査は大事）

https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.219.4542&rep=rep1&type=pdf

https://www.fei.stuba.sk/buxus/docs/2017/autoreferaty/Fabsic_autoref.pdf

https://eprint.iacr.org/2012/409.pdf

最新
https://arxiv.org/pdf/1904.12215.pdf

LDPCを使えばn/2くらいの重みでも訂正できる。
つまりアリスの秘密のベクトルの重みwt(xb)=wt(k)=n/2とすると、
仮にアリスがxbを使って復号したとしても、エラーパターンのハミング重み自体には
変化が少なく（互いに消しあったりするため）、その結果x0⊕x1⊕k,とkの違いは見分けられなくなる。
しかし従来の攻撃法には低密度パリティチェック符号は弱かった。
そこで上記の論文で採用された方式を使って公開鍵の安全性を高めたうえで、QC-LDPCを使い
この方式を復活させることを思いついた。

しかしこのような攻撃が見つかっている。

https://eprint.iacr.org/2017/494.pdf

対抗策

https://arxiv.org/pdf/1808.01945.pdf

