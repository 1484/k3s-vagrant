# k3s-vagrant
k3s環境をVagrantを用いて構築します。virtualboxを使われている方が多いですがlibvirtで動作する様に書いています。その関係でsynced_folderにnfsを使いたいので環境としてnfsも必要です。

## 動作確認環境
 - Vagrant 2.2.6
 - KVM(libvirt)
 - nfs-server

## 既知事象
`vagrant up` をした際にMaster -> Node の順に構築されれば問題ないのですがまだそこのコントロールができておらず、`vagrant up`で失敗します。
仕方ないので`vagrant provision`にて再構築を行う事で環境構築が完了する事が多いです。provisioningの順番を指定する方法誰か教えてください。
