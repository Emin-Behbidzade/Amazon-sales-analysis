# Amazon Satış Analizi

## Dataset
- Mənbə: Kaggle — Amazon Sale Report
- 128,975 sifariş, 24 sütun
- Hindistan Amazon platformasının satış datası (Mart–İyun 2022)

## Nə etdim

**Məlumat Təmizliyi**
- Lazımsız sütunları sildim: promotion-ids, fulfilled-by, ASIN, SKU — bunlar analiz üçün heç bir dəyər daşımırdı
- Amount sütununda 7,795 boş sətiri sildim — məbləği olmayan sifariş satış deyil, analiz üçün yararsızdır
- ship-city/state-də 33 boş sətir var idi — ümumi həcmə nisbətən əhəmiyyətsizdir, olduğu kimi saxladım
- Date sütununu datetime formatına çevirdim

**Niyə mean deyil, median?**
Gəlir və məbləğ sütunlarının paylanması skewed idi — yəni bir neçə çox böyük dəyər ortalama mean-i yuxarı çəkir. Bu halda median daha düzgün mərkəzi göstərici verir.

## Analiz Nəticələri
- Aylıq trend: Aprel 28.8M INR ilə zirvəyə çatdı, İyuna qədər ardıcıl azaldı
- Mart datası tam deyil — yalnız son bir neçə günü əhatə edir, trende daxil etmədim
- Ən çox satan kateqoriya: Set (39.2M INR), ardınca Kurta (21.3M INR)
- Ləğvetmə dərəcəsi: 8.8% — 128,975 sifarişdən 10,766-sı ləğv edilib
- Ən güclü region: Maharashtra (13.3M INR) — ümumi gəlirin 16%-i

## Əsas İnsight-lar
- Maharashtra tək başına ümumi satışın 16%-ni verir — kampaniya üçün prioritet region
- Set kateqoriyası Kurta-dan demək olar 2 dəfə çox satır — stok planlamasında bu nəzərə alınmalıdır
- 8.8% ləğvetmə dərəcəsi biznes üçün ciddi siqnaldır — sonrakı mərhələdə səbəb analizi aparıla bilər

## İstifadə Etdiyim Alətlər
- Python (pandas, matplotlib)
- Power BI — loan_grade slicer ilə interaktiv dashboard

## Dataset
- Mənbə: [Amazon Sale Report — Kaggle](https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset)
- 128,975 sifariş, 24 sütun
- Hindistan Amazon platformasının satış datası (Mart–İyun 2022)
- Orijinal fayl ölçüsü GitHub limitini keçdiyi üçün yüklənməyib, yuxarıdakı linkdən endirmək olar
