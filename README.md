# Taiko-Node

<h1 align="center"> Taiko </h1>


<h1 align="center"> Donanım </h1>

> Hetzner'i 3$ sunucuyu kullandım. 

```
2 CPU 
4 GB RAM 
50 GB SSD 
```

<h1 align="center"> Kurulum </h1>

```sh
# Komutları tek tek girelim.
sudo apt update 
sudo apt upgrade
apt install docker-compose
apt install git
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin

# Repoyu klonlayıp dizine girelim.
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node

#Ayrı screende çalıştıracağız:
screen -S taiko
```

<h1 align="center"> Dikkat edilmesi gereken nokta </h1>

> Alchemy hesabımdan taiko için bir dApp oluşturdum.
>> Bu dApp, Ethereum - Sepolia zinciri olacak.



> Daha sonra View key kısmından key bilgilerimi aldım:



> Altta ki komutlar ile `.env` içine girdim.

```sh
cd simple-taiko-node
cp .env.sample .env
nano .env
```

> L1_ENDPOINT_HTTP= Bu kısıma Alchemyden aldığınız HTTPS adresini yazıyorsunuz

> L1_ENDPOINT_WS= Bu kısıma Alchemyden aldığınız WSS adresini yazıyorsunuz

> L1_PROVER_PRIVATE_KEY= Bu kısıma Metamask Private keyinizi yapıştırıyorsunuz

> CTRL X Y ile çıkıyoruz.



<h1 align="center"> Node'u çalıştırma </h1>

> Faucet Linki https://sepoliafaucet.com/
 
``` 
# Node'u çalıştırın
docker compose up
```
