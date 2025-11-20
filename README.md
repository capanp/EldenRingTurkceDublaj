# Elden Ring Ses Modlama ve Değiştirme Rehberi
Bu repoda elden ringteki tüm sesleri nasıl değiştirebileceğinizi öğreneceksiniz gerekli olan tüm araçlar repoda bulunur

Reponun ana amacı elden ringe herhangi bir dilde dublaj yapmanıza olanak sağlamak.

##Geliştirici ortamı kurulumu
Reponun kaynak kodunu veya varsa son sürümünü indirip bir dosyaya çıkarın.
###Ön Gereklilikler
 - [Ffmpeg](https://www.ffmpeg.org/download.html)
 - [Python](https://www.python.org/downloads/)
 - [Wwise 2019](https://www.audiokinetic.com/en/download/)

 - [UXM Selective Unpacker](https://github.com/Nordgaren/UXM-Selective-Unpack/releases/tag/2.4.2)

##Dosyaları ayıklama
Geliştirici ortamanızı bitirmek için oyunun parçalanmış seslerine ihtiyacımız var [UXM Selective Unpacker](https://github.com/Nordgaren/UXM-Selective-Unpack/releases/tag/2.4.2) aracı ile elden ringin **tüm dosyalarını parçalayın** (sadece sesleri seçerseniz tüm sesler çıkamaz .bnk'lar ilk ayırmada temiz ayrılmak zorunda daha sonra silebilirsiniz).

Şimdi tüm işimiz ./game/sd/ klasörünün içinde, ilk baş buranın ne olduğunu anlayalım iki adet sd nin içinde iki adet klasörü bulunur bir klasör sadece sfx tarzı ses içeriklerini içerirken diğeri npc vb. canlı varlıkların her türlü sesini içerir yani bir dublaj yaptığınızı varsayarsak ses içereni seçmeliyiz

İçinde ./wem , vcmain, vc100,vc101, vcXXX vb. bir dosya yolu izliyorsa npc seslerindeki dosyadasınız demektir. 

Şimdi dosyaları dinlenilebilir yapma zamanı, npc dosyalarını kopyalayıp proje klasörümüzdeki ./sounds konumuna getiriyoruz.

eklediğimiz bütün dosyaları ve ./wem klasörünü seçip sürükleyip **bnk2json.exe** nin üzerine bırakıyoruz.(bu biraz zaman alacak kahve yapın).

Bittiğinde tonla klasör ve içlerinde wem dosyaları görüyorsanız, tebrikler kurulumu başarıyla tamamladınız..

##Kullanmaya başlama
Şimdi geliştirici ortamını anlatmadan önce nasıl sesleri bulup dinleyebileceğiniz anlatmılıyım;

./wemmap/wem_talk_map_v.0.0.2.csv yazı dosyasını açın ve istediğiniz ses satırlarını kopyalayın daha sonra projenini ana konumuundaki cutscene.md nin içine yapıştırın.
proje konumunda "python ./collect_wems.py" komutunu yürütün (seçtiniğiz ses dosyalarının wem dosyaları ./input/wem e geldi) şimdi bunları dinlenilebilir yapmak için "python ./wem2wav.py" komutunu yürütün.

Seçtiğiniz sesler ./output/wem_output konumunda .wav olarak bulunuyor oradan dinleyebilirsiniz.

##Modlamaya başlama




