# This repository is no longer maintained

git clone https://github.com/lede-project/source

cd source

echo "src-git cups https://github.com/Gr4ffy/lede-cups.git" >> feeds.conf.default

./scripts/feeds update -a

./scripts/feeds install -a

make menuconfig (set Network->Printing->cups as "M")

make

copy /source/bin/packages/<arch>/cups/*.ipk to machine & opkg install 
