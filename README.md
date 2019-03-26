# UbuntuNetworkFix


1 - Instalar o aptitude para corrigir possiveis erros de dependencias/Install the aptitude to fix possibles dependency errors

```sh
$ sudo apt-get install aptitude
```

2- Baixar todos os pacotes, acessar a pasta em que fez o download dos arquivos e instalar por meio do comando: / Download all packages, open the folder where the files downloaded and install by the command:


```sh
$ sudo dpkg -i ca-certificates_20170717_16.04.1_all.deb && sudo dpkg -i libreadline6_6.3-8ubuntu2_amd64.deb && sudo dpkg -i libssl1.0.0_1.0.2g-1ubuntu4.13_amd64.deb && sudo dpkg -i libssl-dev_1.0.2g-1ubuntu4.13_amd64.deb && sudo dpkg -i ocs-url_3.1.0-0ubuntu1_amd64.deb && sudo dpkg -i openssl_1.0.2g-1ubuntu4.13_amd64.deb && sudo dpkg -i wpasupplicant_2.4-0ubuntu6.3_amd64.deb
```

3- Em caso de erros em algumas dependências que não estão instaladas, dê o seguinte comando e repita o comando do passo 2 até que não haja mais erros no downgrade: / In case of errors in some dependencies, do the command and repeat the command of step 2 until there are no further downgrades errors:

```sh
$ sudo aptitude safe-upgrade
```

4- Confira se todos pacotes estão na versão correta e marque os downgrades realizados para que não sejam atualizados com o seguinte comando: / check if all packages are in the correct version and mark the downgrades for they aren't update:

```sh
$ sudo apt-mark hold wpasupplicant:amd64 && sudo apt-mark hold openssl:amd64 && sudo apt-mark hold ocs-url:amd64 && sudo apt-mark hold libssl-dev:amd64 && sudo apt-mark hold libc-bin:amd64 && sudo apt-mark hold libreadline6:amd64 && sudo apt-mark hold ca-certificates:all
```
