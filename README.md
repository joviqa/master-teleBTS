# Proyecto de Central Telefonica BTS - EPIT
Guia y Archivos de configuracion para OpenBTS


1.- Actualizar el sistema e instalar paquetes necesarios

```
sudo apt update
sudo apt upgrade
sudo apt install git vim build-essential asterisk asterisk-mysql asterisk-config libuhd4.6.0 uhd-host libuhd-dev sqlitebrowser
```

2.- Descargar el directorio GIT

```
git clone https://github.com/joviqa/master-teleBTS
cd master-teleBTS
```

3.- Descargar el Repositorio de OpenBTS

```
git clone https://github.com/PentHertz/OpenBTS.git
cd OpenBTS
git checkout 5.1.0
```

4.- Agregar archivos y compilar OpenBTS

```
cp ../preinstall .
chmod +x preinstall
./preinstall
./autogen.sh
./configure --with-uhd
make -j4

```

5.- Instalar OpenBTS

```
sudo make install
sudo ldconfig
```



