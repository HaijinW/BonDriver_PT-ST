オリジナルのBonDriver_PT(人柱版３)との使用する上での相違点

・BonDriver_PT-S.ChSet.txtのTSID項目に0～7の値を指定するとチューナーからTSIDを
  抜き取って下位3ビットがその値と一致するTSIDを持つストリームを自動選択します。
  トランスポンダの再編などによりチャンネル情報が変更された場合にチャンネルファ
  イルのTSIDを実質一々書き換える必要がなくなりアプリケーション側のチャンネルス
  キャンだけで事が足りるようになります。
  (Described by 2020 LVhJPic0JSk5LiQ1ITskKVk9UGBg)

・BonDriverのバイナリファイルはS用もT用も同一です。
  名前が「BonDriver_PT-T.dll」あるいは「BonDriver_PT-Tx.dll」の場合はT用として、
  「BonDriver_PT-S.dll」あるいは「BonDriver_PT-Sx.dll」の場合はS用として動作するので、
  dllファイルをコピーし、名前を変更して使用して下さい。

・iniファイルの中に「PTver」の項目が増えています。
  このBonDriverをPT2で使用する人は「2」を、PT1で使用する人は「1」を指定してください。
  この値は実質ほぼ利用されていないので、EDCBで使用する場合以外は多分変更する必要はありません。
  (EDCBでは設定ファイルの名称にBonDriverのファイル名だけでなくこの値も使用している為、
   ここが間違っていると既存の設定ファイル(XXXX.ChSet4.txt)が読み込めなくなります。)
