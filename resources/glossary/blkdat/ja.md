---
term: BLK*.DAT

---
ブロックチェーンの生のブロックデータを格納するビットコインコアのファイル名。各ファイルは、その名前に含まれる一意の番号によって識別される。したがって、ブロックは時系列順に記録され、blk00000.dat というファイルから始まる。このファイルが最大容量に達すると、次のブロックはblk00001.datに記録され、次にblk00002.datというように記録される。各blkファイルの最大容量は128メガバイト（MiB）で、これは134メガバイト（MB）強に相当する。これらのファイルはバージョン0.8.0以降、`/blocks`フォルダに移動された。