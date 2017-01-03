

#Install Sbort di CentOS

<p align="center">
  <img src="/img/06.png" width="400px">
</p>


Pertama-tama pastikan paket yang kita butuhkan telah disiapkan
Libpcap
Daq
Libdnet
Pertama install pcap
Tar xvzf libpcap-1.1.1.tar.gz
Cd libpcap-1.1.1
./configure –prefix=/usr/local
make
make install
Selanjutnya install paket daq, sebelumnya copykan dulu libary pcap ke /usr/lib
cp/usr/local/lib/libpcap.a /usr/lib/
tar xvzf daq-0.5.tar.gz
cd daq-0.5
./configure –prefix=/usr/local
make
make install
Selanjutnya install paket dnet
Dan terakhir install snortnya
tar xvzf snort-2.9.0.4.tar.gz
cd snort-2.9.0.4
./configure --prefix=/usr/local/ --sysconfdir=/usr/local/etc/ --sbindir=/usr/local/sbin/ --with-mysql --with-libpcap-libraries=/usr/lib/libpcap1/lib/ --enable-dynamicplugin --enable-build-dynamic-examples --with-dnet-libraries=/usr/lib/ --with-daq-libraries=/usr/lib/daq/ --with-daq-includes=/usr/include/ --enable-ipv6 --enable-gre --enable-mpls --enable-targetbased --enable-decoder-preprocessor-rules --enable-ppm --enable-perfprofiling --enable-zlib --enable-active-response --enable-normalizer --enable-reload --enable-react --enable-flexresp3
