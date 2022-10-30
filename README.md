<h1 align="center">Manta Network Trusted Setup (Güvenli  Kurlum)

## Manta Network, kısaca zkSNARKs üzerine inşa edilmiş blockchain projeleri için gizliliği sağlayan bir gizlilik protokolüdür. Trusted Setup Kurlumu için [buraya](https://docs.manta.network/docs/concepts/TrustedSetup) da bakabilirsiniz.

## Video [Linki](https://youtu.be/jf5dvWblYek) 

## Manta Network için Sunucuyu nerden nasıl alacağınızı bilmiyorsanız node eğitim serimizi izleyebilirsiniz. [Node Eğitim Serisi](https://www.youtube.com/playlist?list=PLKxGUfdcj7MVXls2OvTpwx6CnpVJN685w)

![image](https://docs.manta.network/img/guides/trusted-setup-stages.svg)
## Manta Network için iki tane aşama olacak şuan ilkini yapacağız bunun karşılığında NFT verilecek ilerleyen zamnlarda 2. aşama açılınca onuda yapacağız.

### Sistem Gereksinimleri
 - kurulum için sistemin özellikleri çok önemli değil, zaten bitirdikten sonra vps sıfırlayacağız dileyen arkadaşlar silebilir farklı bi kurulum daha gelecek ondan sonra sileriz.
 - Ubuntu 20.04
 - 2 CPU
 - 4GB RAM
 - disk boyutu önemsiz
 # 1. kurulum için 2 tane seçeneğimiz bulunuyor ilki otomatik kurlum ikincisi ise manuel kurulum eğer otomatik kurlumda hata alırsanız manuel kurulumu uygulayın.

<h1 align="center">Otomatik Kurulum

  ## Root yetkisi almak için aşağğıdaki kodu giriyoruz bazı sunucularda bunu sürekli girmemiz gerekiyor. eğer bunu girmezseniz yazdığınız kodun başına sudo komutunu yazarkata devam edebilirsiniz ancak karışıklık olmaması için aşğıdaki komutu yazmanızı tavsiye ederim. ( root: Windows cihazlarda olduğu gibi yönetici olarak çalıştırmamıza, yani bize yetki veren bir komuttur.)
  ```
  sudo su
  cd
  ```

 ## Aşşağıdaki komutlarla sunucumuzdaki güncellemeleri, yükseltmeleri kontrol ediyoruz, sondaki -y işareti gelen onay işlemlerini otamatik olarak onaylanmasını sağlayacaktır.

  ```
 sudo apt update && sudo apt upgrade -y
  ```

 ## bu komut bizim sırayla gireceğimiz komutları tek kod olarak almamızı sağlar sh uzantılı dosyayı indirerek ne çalıştırıldığını görebilirsiniz, bash script olarak yazılmıştır. Mantadan direk alıntı

 ```
curl --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/Manta-Network/manta-rs/main/tools/install.sh | sh
 ```

  ## Kurulum işelmleri tamamlandıktan sonra source ile değişikliklerin sistem tarafından tanınmasına sağlarız, yani kurlumumuz bir nevi kontrol eidlir yapılandırma da denilebilir.
   ```
source ~/.profile
 ```
  
   ## Şimdi kayıt işlemlerini yapıyoruz. Buraya twitter kullanıcı adımızı yazıyoruz başında "@" işareti koymadan giriyoruz. Sonrasında mail adresimizi giriyoruz videodan takip edebilirsiniz.

<h1 align="center"> Manuel Kurulum


  ## Root yetkisi alıyoruz.
  ```
  sudo su
  cd
  ```

 ## Temel gereksinimler sunucu güncelleme

  ```
 sudo apt update && sudo apt upgrade -y
  ```

 ## Sonrasında aşağıdaki komutları sırasıyla giriyoruz.

 ```
sudo apt install git pkg-config build-essential libssl-dev curl jq
 ```
 ```
curl https://sh.rustup.rs -sSf | sh -s -- -y
 ```
 ```
source $HOME/.cargo/env
 ```
 ```
git clone https://github.com/Manta-Network/manta-rs.git
 ```

 ```
cd manta-rs
 ``` 
 ```
cargo run --release --package manta-trusted-setup --all-features --bin groth16_phase2_client register
 ```  
  
## Şimdi kayıt işlemlerini yapıyoruz Buraya twitter kullanıcı adımızı yazıyoruz başında "@" işareti koymadan giriyoruz. Sonrasında mail adresimizi giriyoruz videodan takip edebilirsiniz. burda size verdiği bilgileri not almayı unutmayın formda kullanacağız ve saklayın.

## Kayıt formunu doldurmayı unutmayalım. [Buradan](https://mantanetwork.typeform.com/TrustedSetup) kayıt formuna ulaşabilirsiniz. ayrıca [Discord](https://discord.gg/mantanetwork) Sunucularından katılmayı unutmayın.

  ## Eğer polkadot cüzdanını kullanmayı bilmiyorsanız videodan takip edin formda sizden  KMA adresinizi vermenizi isteyecek, bunun için polkadotjs cüzdana sahip olmanız gerekiyor.
 

