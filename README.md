
# これは 仮想的な11bit計算機用のエミュレータです。

概要
  仮想的な11bitのCPUをエミュレートしてみます。

  命令セットは、
   ../asm11/instruction_set.h
  を参照してください。

  アドレスバス、データバス、レジスタサイズともに11bitです。

  命令コードは  16bitで、
  内訳は上位 5bit(instruction_set.h) + 下位11bit(オペランド)です。


# 11bit計算機用とは、なんだったのか？

参考ページ：
  https://github.com/iruka-/ATMEL_AVR/blob/master/md/2014-08.md

簡単な説明
  FullTr-11 の命令セットを真似た計算機です（あくまでも概要から推測したもので、実在しません）
  
  FullTr-11 は、全て2SC1815のようなディスクリートトランジスタのみで構成された計算機です。

  FullTr-11 を使用して、円周率を少し計算するところまで、エミュレートしています。

なお、私は  FullTr-11 の購入者でもありませんし、作者との面識もありません。


-----------------------------------------------------
お約束
-まだ完成品ではありません。
-テストパタンはありあわせです。
-コマンドライン上から実行します。
-実在する11bit CPUと動作が異なる場合があります。


補足
- JMP 自分自身のアドレス、という命令を実行するとエミュレーション
  を終了します。

- 

-----------------------------------------------------
ＴｏＤｏ

-----------------------------------------------------
ビルド方法:

	Windows上でのビルド＝　MinGW-gcc （www.mingw.org）と make を使用します。

	Linux 上でのビルド ＝　普通のgcc と make を使用します。


-----------------------------------------------------
ソフトウェア配布ライセンス

The MIT License
 Copyright (c) 2012  AVRetc

以下に定める条件に従い、本ソフトウェアおよび関連文書のファイル（以下「ソフトウェア」）の複製を取得するすべての人に対し、ソフトウェアを無制限に扱うことを無償で許可します。これには、ソフトウェアの複製を使用、複写、変更、結合、掲載、頒布、サブライセンス、および/または販売する権利、およびソフトウェアを提供する相手に同じことを許可する権利も無制限に含まれます。 

上記の著作権表示および本許諾表示を、ソフトウェアのすべての複製または重要な部分に記載するものとします。 

ソフトウェアは「現状のまま」で、明示であるか暗黙であるかを問わず、何らの保証もなく提供されます。ここでいう保証とは、商品性、特定の目的への適合性、および権利非侵害についての保証も含みますが、それに限定されるものではありません。 作者または著作権者は、契約行為、不法行為、またはそれ以外であろうと、ソフトウェアに起因または関連し、あるいはソフトウェアの使用またはその他の扱いによって生じる一切の請求、損害、その他の義務について何らの責任も負わないものとします。 


-----------------------------------------------------
