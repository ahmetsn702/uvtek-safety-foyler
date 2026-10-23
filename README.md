# UVTEK Kartezyen Robot Sprey Boyama Makinesi: Safety 4.0 Lab Föyleri (1–4)

**Ad Soyad:** Ahmed Hüsrev Sayın
**Grup:** Gece - 225541103

Safety 4.0 Bootcamp'teki ilk 4 laboratuvar föyünü kendi seçtiğimiz makine, **UVTEK Kartezyen Robot Sprey Boyama Makinesi** için doldurduk.

## Makine

X-Y-Z eksenli kartezyen robot, boyanacak parçanın üzerinde sprey tabancasını gezdirir. Parçalar konveyörle kabine girer. Kabin egzoz fanı ve filtrelerle havalandırılır.

| Bileşen | Görev |
|---|---|
| PLC + HMI | Eksen hareketi, boya programı (reçete), konveyör |
| Robot kontrolörü + servo sürücüler | X-Y-Z eksenleri |
| Sprey tabancası + boya pompası | Boya uygulama |
| Safety PLC | E-stop, kabin kapı kilidi, egzoz izleme → STO |
| Uzak servis erişimi | Üreticinin uzaktan bakım / güncelleme bağlantısı |

**Tehlikeler:** Hareketli eksenler (çarpma, sıkışma), yüksek basınçlı tabanca (boyanın cilde enjekte olması), solvent buharı (yangın).

## Föyler

| # | Föy | Çıktı | Dosya |
|---|---|---|---|
| 1 | Safety Architecture | Safety Function Map | [Lab1_Safety_Architecture.pdf](foyler/Lab1_Safety_Architecture.pdf) |
| 2 | IEC 62443 Mini Workshop | Zone / Conduit Diagram | [Lab2_Zone_Conduit.pdf](foyler/Lab2_Zone_Conduit.pdf) |
| 3 | Threat & Risk + Risk Matrix | Risk Register | [Lab3_Risk_Register.pdf](foyler/Lab3_Risk_Register.pdf) |
| 4 | Secure Remote Access | Secure Architecture | [Lab4_Secure_Remote_Access.pdf](foyler/Lab4_Secure_Remote_Access.pdf) |

Dört föyün tek dosya hali: [UVTEK_Foyler_1-4.pdf](UVTEK_Foyler_1-4.pdf)

## Özet

- **Emniyet fonksiyonu:** Kabin kapısı açılınca ya da E-stop'a basılınca eksenler ve tabanca durur (STO).
- **Zone'lar:** Safety, Kontrol, Mühendislik, DMZ, Ofis/IT. Kontrol → Safety geçişi sadece okuma.
- **En kritik risk:** Uzak servis üzerinden Safety PLC'de kapı kilidinin kapatılması (L2 × S3 × E3 = 18, Kritik).
- **Uzak erişim:** Jump server + VPN + MFA + kişisel hesap + tam oturum kaydı + varsayılan kapalı.
- **Bağımsızlık gereksinimi:** Kontrol sistemi veya ağ ele geçirilse bile emniyet fonksiyonu eksenleri ve tabancayı durdurabilmeli.

> Bu bir eğitim çalışmasıdır, resmî denetim değildir.
