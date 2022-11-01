These blk files were created with the following process. Be sure to replace the paths in the cfg files to suit your environment:

> ./bitcoin/contrib/linearize/linearize-hashes.py hashes.cfg > hashes.txt

> ./bitcoin/contrib/linearize/linearize-data.py data.cfg

These files can be used to test, with for example:

> mkdir -p /tmp/btc && gdb --tui --args ./src/qt/bitcoin-qt -debug -logthreadnames -datadir=/tmp/btc -prune=550 -loadblock=/linearblocks/blk{00000..00014}.dat -connect=0
