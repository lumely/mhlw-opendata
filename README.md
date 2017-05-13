## なにこれ
厚生労働省が2017年5月10日に公表した，[労働基準関係法令違反に係る公表事案](http://www.mhlw.go.jp/kinkyu/dl/170510-01.pdf)のデータをクリーニングしてCSVにしたものです

## なぜこんなことをしたの？
はてブでCSVにしろというコメントがたくさんあったことと，[同省が2017年3月30日に公開した文書](http://www.mhlw.go.jp/kinkyu/dl/170510-02.pdf)によれば，公開後1年で消すとなっていたので，貴重なデータが失われることに危機感を覚え，約2時間かけてやってみました

## こんなことして大丈夫なの？
[同省は，同Webサイトのコンテンツの利用について利用規約を定めています](http://www.mhlw.go.jp/chosakuken/)．本加工・及び再公開は当該規約に則ったものです

## 出典
労働基準関係法令違反に係る公表事案（厚生労働省）[http://www.mhlw.go.jp/kinkyu/dl/170510-01.pdf](http://www.mhlw.go.jp/kinkyu/dl/170510-01.pdf)を加工して作成しました

### 加工内容
- 全角のアラビア数字を半角に統制した
- 和暦を西暦に統制した
- 年月日は `` yyyy-mm-dd ``で統制した
- `` 事案ID ``列，`` 担当労働局 ``列，`` 最終更新日 ``列及び`` 出典 `` 列を追加した
  - `` 事案ID ``は最初を1とし，元データの並び順に対し上から1ずつインクリメントする値
  - `` 出典 ``は元データのURL
- `` 企業・事業場名称 ``列を`` 法人名称カナ略語 ``列と`` 企業・事業場名称 ``列に分割した
- `` 所在地 ``列を`` 所在都道府県 ``列と``所在市区郡町村``列に分割した
- ~~`` 違反法条 `` 列においては `` | `` をデリミタにした~~
- `` 違反法条 ``列は`` 違反法条1 ``と`` 違反条項 ``列に分割し，1列1法条・条項となるように`` 違反法条5 ``，`` 違反条項5 ``列まで作成した
  - 2017年5月10日に公表された事案では1次案につき最大3法条が紐付いていたが，今後の拡張を考え5法条まで対応可能とした
- `` その他参考事項 `` 列は`` 送検年月日 ``列，`` 不起訴(嫌疑不十分)年月日 ``列，`` 不起訴年月日 `` 列に分割した
- `` n,nnn万円 `` という表記は `` nnnn万円 `` に修正した
- `` 労基法 `` は `` 労働基準法 ``に，`` 安衛法 ``は`` 労働安全衛生法 ``に，`` 安衛則 ``は`` 労働安全衛生規則 ``にそれぞれ修正した
- `` 労働安全衛生施行令 ``は`` 労働安全衛生法施行令 ``に修正した
- `` 労働安全衛生規則41条 ``は`` 労働安全衛生規則第41条 ``に，`` 労働基準法62条 ``は`` 労働基準法第62条 ``にそれぞれ修正した
- `` 川崎市高津区 ``は `` 神奈川県川崎市高津区 ``に，`` 神戸市兵庫 ``は`` 兵庫県神戸市兵庫区 ``にそれぞれ修正した
- ``（株）大昌◆工所 ``は``（株）大昌鉄工所 ``に修正した
  - ◆は金へんに矢
  
## 利用規約について
本データの利用規約は，[厚生労働省の利用規約](http://www.mhlw.go.jp/chosakuken/)と同一のものとします．
本データの利用にあたり，lumelyに確認等は一切不要です．

### 注意・免責事項
- 本データの加工は細心の注意をもって行いましたが，過失による加工ミスにより，[元データ](http://www.mhlw.go.jp/kinkyu/dl/170510-01.pdf)と異なる箇所が存在する可能性があります．その場合，ただちに修正しますので，ご連絡頂ければ幸いです．
- 本加工データを用いて行う一切の行為に対し，lumelyは何ら責任を負うものではありません
- 加工ミスを発見した場合，予告なく変更，移転，削除などを行うことがあります
- 予告なくさらに正規化などのより機械処理が容易な形式に変更することがあります

### 今後の予定
LODにしてLODチャレンジに出したいですね．アプリ込みで
