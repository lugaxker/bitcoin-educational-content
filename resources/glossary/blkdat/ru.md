---
term: BLK*.DAT

---
Название файлов в Bitcoin Core, в которых хранятся необработанные данные блока блокчейна. Каждый файл идентифицируется по уникальному номеру в его имени. Таким образом, блоки записываются в хронологическом порядке, начиная с файла blk00000.dat. Когда этот файл достигает своего максимального объема, следующие блоки записываются в файл blk00001.dat, затем blk00002.dat и так далее. Максимальный объем каждого файла blk составляет 128 мегабайт (MiB), что эквивалентно чуть более 134 мегабайтам (MB). Начиная с версии 0.8.0 эти файлы были перемещены в папку `/blocks`.