---
用語BIP149

---
BIP9によるSegWitの初期展開が2017年11月15日までにアクティブ化に失敗した場合、`LOT=true`を用いたBIP8アクティブ化方式によるSegWit（BIP141、BIP143、BIP147）の新たな展開に関するShaolin Fry氏による提案。シグナリングの失敗によってアクティベーションが放棄されるBIP9方式とは異なり、BIP149は、マイナーたちが95%のシグナリングのしきい値に達したかどうかにかかわらず、2018年7月4日にSegWitをアクティベーションすることを目指しました。11月から7月までの8カ月間、ノードはBIP149を実施する機会があり、マイナーのアクティベーションが発生しなかった場合（UASF）、ネットワークの経済的多数派によるSegWitのアクティベーションを確保することができました。2018年7月4日以降に最初の難易度調整に達すると、アクティベーションは`LOCKED_IN`に移行し、次の調整サイクルでSegWitがアクティベートされたことでしょう。ユーザーまたは大多数のマイナーによって強制されるSegWitの活性化を計画していたBIP148とは異なり、BIP149は、BIP8の原則に従った、明らかに攻撃的であることに変わりはないものの、より緩やかで慎重な活性化方法を示唆していた。BIP148はブロックチェーンの分裂との衝突を予期していたが、BIP149はマイナーの意図的な行動（インセンティブなし）を除き、SegWitのシグナルを出さないブロックを受け入れることでこの可能性を回避した。したがって、BIP149はBIP148よりも衝突の少ないSegWit起動メカニズムであり、システムにとってより緩やかでリスクの少ない採用が支持された。BIP148もBIP149も最終的には実装されず、SegWitはMASFを通じて、特にBIP91の衝動の下で活性化された。