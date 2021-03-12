---
title: Erän tasaus
description: Tässä ohjeaiheessa käsitellään erän tasausprosessia.
author: johanhoffmann
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c1f52239b2050425c37a8130507e689b29205a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966552"
---
# <a name="batch-balancing"></a>Erän tasaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään erän tasausprosessin tukea.

Lisätietoja saa katsomalla [erän tasausta käsittelevän videon](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).

Erän tasausprosessissa tuotantoerässä käytettyjen ainesosien määrä lasketaan valittujen tuote-erien vaikuttavien ainesosien pitoisuuden perusteella.

## <a name="products-that-have-an-active-ingredient"></a>Tuotteet, joissa on vaikuttava ainesosa

Tuote voidaan määrittää vaikuttavan ainesosan pitoisuuden mukaan. Tuotteen vaikuttava ainesosa mallinnetaan tuotekohtaisella erämääritteellä, jolla on minimiarvo, maksimiarvo ja tavoitetaso.

Erämääritteen tavoitetaso vastaa tuotteen vaikuttavan ainesosan arvioitua prosenttiosuutta. Minimi- ja maksimiarvot vastaavat hyväksyttyjä poikkeamia tavoitetasosta. Niitä voidaan käyttää esimerkiksi tuotteen vastaanotossa erien hyväksyttävänä toleranssina.

Tuotteella voi olla vain yksi vaikuttava ainesosa. Kun tuotteelle määritetään vaikuttava ainesosa, ensimmäiseksi on määritettävä tuotekohtainen erämäärite. Sen jälkeen määritteen voi liittää tuotteen perusmääritteenä.

Tuotetasolla on lisäksi määritettävä, miten tuote-erän vaikuttavan ainesosan taso on kirjattava: osana oston vastaanottoprosessia vai laatutilausprossin osana.

Perusmääritteen liittämiseen tuotteeseen tarvitaan seuraava asetus:

- Tuotteen on oltava eräohjattu. Tuotteesta tulee eräohjattu, kun sellaiselle tuotteelle määritetään seurantadimensioryhmä, jolla on aktiviinen erädimensio.

- Ainesosatasot ilmaiseva määrite on oltava määritetty tuotteen tuotekohtaiseksi erämääritteeksi.

Erän vaikuttavan ainesosan todellisen arvon hakeminen ja muokkaaminen:
1. Valitse **Inventoinnin- ja varastonhallinta \> Kyselyt ja raportit \> Seurantadimensiot \> Erät**.
1. Valitse eränumero ruudukossa.
1. Avaa toimintoruudussa **Näytä**-välilehti ja valitse sitten **Varastoerämääritteet**.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Ainesosatyypit ja niiden toiminta erän tasausprosessissa

Luodulla reseptirivillä voi olla yksi seuraavista ainesosatyypeistä:

- None
- Aktiivinen
- Kompensoidaan
- Täyttäjä

Tässä osassa käsitellään nyt esimerkkejä, jotka osoittavat, miten kukin ainesosatyyppi toimii. Esimerkit perustuvat seuraavan reseptiin, jonka kokonaiseräkoko on 100 litraa.

| Ainesosan tyyppi | Nimiketunnus | Reseptirivin määrä | Yksikkö |
|---|---|---|---|
| None | A | 20 | litra |
| Käytössä | D | 30 | litra |
| Kompensoidaan | K | 10 | litra |
| Täyttäjä | D | 40 | litra |

Seuraavassa taulukossa on kunkin esimerkin tulosten yleiskatsaus.

| Nimiketunnus | Ainesosan tyyppi | Arvioitu määrä | Täsmäytetty määrä | Aktiivinen määrä | Yksikkö | Perusarvo |
|---|---|---|---|---|---|---|
| A | None | 20 | 20 | | litra | |
| D | Aktiivinen | 30 | 25,71 | 9:00 | litra | 30.00 |
| K | Kompensoidaan | 10 | 14.72 | | litra | |
| D | Täyttäjä | 40 | 39.57 | | litra | |

### <a name="active-ingredients"></a>Vaikuttavat ainesosat

Kun perusmääritteellinen tuote lisätään reseptiriville, sitä kutsutaan reseptin *vaikuttavaksi ainesosaksi*. Kun erätilauksessa on reseptejä, joissa on vaikuttavia ainesosia, niitä voidaan käyttää erän tasausprosessissa. Erän tasausprosessi arvioi reseptin jokaisen ainesosan kohdalla määrän, joka tarvitaan tuotteen valmistamiseen. Määrien arvio perustuu valittujen erien vaikuttavien ainesosien pitoisuuteen.

#### <a name="active-ingredient-example"></a>Vaikuttavan ainesosan esimerkki

Ainesosassa B on perusmäärite X ja sen tavoitetaso on 30. Se sisältyy reseptiin, jossa tarvitaan 30 litraa ainesosaa B tuotteen jokaista 100 litraa kohden. Luotavan erätilauksen eräkoko on 100 litraa. Erätilaus käynnistetään ja erän tasausprosessin aikana käyttäjä valitsee erän ainesosaa B, jonka vaikuttavuustaso on 35. Koska vaikuttavuustaso 35 on suurempi kuin tavoitetaso 30, ainesosan B täsmäytettyä määrää vähennetään käyttämällä vaikuttavuuden arvon suhdetta erän tavoitetasoon, joka sitten kerrotaan arvioidulla määrällä. Täsmäytetyn määrään laskelma:

(30 ÷ 35) × 30 litraa = 25,71 litraa

### <a name="none-ingredients"></a>Ei ainesosia

Kun käytät erän tasausprosessia **ainesosatyypin** ollessa *Ei mitään*, arvioitu määrä ja erätilauksen reseptirivin täsmäytetty määrä on sama.

#### <a name="none-ingredient-example"></a>Ei mitään -ainesosan esimerkki

Ainesosa A on määritetty tyypin *Ei mitään* ainesosaan ja lisätty valmiin tuotteen reseptiin. Reseptin mukaan 100 litraan valmista tuotetta tarvitaan 10 litraa ainesosaa A. Kun erätilaukseen tarvitaan 200 litraa, sekä arvioiduksi määräksi että ainesosan A täsmäytetyksi määräksi lasketaan 20 litraa.

### <a name="compensating-ingredients"></a>Kompensoivat ainesosat

Kompensoiva ainesosa voi joko siirtää tai täydentää tuotteen vaikuttavan ainesosan vaikutusta. Tämän vuoksi kulutetun kompensoivan ainesosan määrä määräytyy tuotteen vaikuttavuuden mukaan:

- **Vastakkainen vaikutus** – jos vaikuttavan ainesosan määrä on odotettua suurempi, kompensoivaa ainesosaa on lisättävä vähemmän.

- **Täydentävä vaikutus** – jos vaikuttavan ainesosan määrä on odotettua pienempi, kompensoivaa ainesosaa on lisättävä enemmän.

Vaikuttavan ainesosan ja kompensoivan ainesosan suhde määritetään **Kompensaatioperiaate**-sivulla.

Määritä ainesosien välinen suhde seuraavasti:

1. Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Reseptit**.
1. Avaa reseptirivi ja avaa sitten **Kompensaatioperiaate**-sivu valitsemalla **Ainesosat**.
1. Valitse ensin kompensaatioperiaatetta vastaava rivi ja sitten kompensoitava vaikuttava ainesosa.

Voit antaa kompensaatioperiaatteessa positiivisen tai negatiivisen kompensointikertoimen määrittämään, miten paljon kompensoidaan ja onko periaate vastakkainen vai täydentävä. Positiivinen kerroin ilmaisee täydentävän vaikutuksen ja negatiivinen kerroin ilmaisee vastakkaisen vaikutuksen.

#### <a name="compensating-ingredient-example"></a>Kompensoiva ainesosa -esimerkki

Ainesosa B on vaikuttava ainesosa, jonka perusmäärite on X ja tavoitetaso 30. Se sisältyy reseptiin, jonka mukaan 100 litraan tuotetta tarvitaan 30 litraa ainesosaa B. Ainesosa C on kompensoiva ainesosa ja sen määrä 10 sisältyy samaan reseptiin. Kompensaatiokerroin 1,10 määritetään kompensaatioperiaatteeksi. Tämän vuoksi kompensoitavan ainesosan täsmäytettyä määrää vähennetään vaikuttavan ainesosan täsmäytetyn määrän ja arvioidun tarvittavan määrän erotuksella, joka kerrotaan luvulla 1,10.

*Vaikuttavan* ainesosatyypin esimerkissä tarvittava vaikuttavan ainesosan täsmäytetyksi määräksi laskettiin 25,71 ja arvioiduksi tarvittavaksi määräksi 30. Tässä tapauksessa kompensoivan ainesosan täsmäytetty määrä lasketaan seuraavasti:

1. Arvioidun ja täsmäytetyn määrän erotuksen laskeminen:  
    25,71–30=–4,29

1. Tulos kerrotaan kompensointikertoimella:  
    4.29×1,10 =–4,72

1. Arvioidusta kompensointimäärästä vähennetään –4,72 ja sen mukaan lasketaan täsmäytetty kompensointimäärä:  
    10–(–4,72)=14,72

Koska 1,10 on positiivinen kompensaatiokerron, kompensaatioperiaatteen vaikutus on täydentävä. Tässä tapauksessa vaikuttavan ainesosan vaikutus on odotettua suurempi. Tämän vuoksi kompensoivaa ainesosaa tarvitaan enemmän.

### <a name="filler-ingredients"></a>Täyteainesosat

*Täyteainesosa* on neutraali ainesosa, jonka avulla saavutetaan toivottu määrä valmista tuotetta. Täyteainemäärien säädöt lasketaan vakiomäärään verrattavan vaikuttavan ainesosan ja kompensoivan ainesosan vaihtelujen perusteella.

#### <a name="filler-ingredient-example"></a>Täyteainesosan esimerkki

Olet luonut reseptin tuotteelle, joka sisältää ainesosat A, B, C ja D. Reseptin koko on 100 litraa. Olet laskenut *Täyteaine*-ainesosatyyppiä lukuun ottamatta kaikkien yhdellä rivillä käytettävien ainesosatyyppien täsmäytetyn määrän.
Täyteainesosan täsmäytetty määrä lasketaan 100 litran eräkoon ja ainesosien A, B ja C summan välisenä erotuksena.

100–(20+25,71+14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Erän tasausprosessi

Erän tasausprosessi suoritetaan **Erän tasaus** -sivulla.
Valitse ensin **Kustannushintojen hallinta \> Erätilaukset** ja sitten **Prosessi**-välilehdessä **Erän tasaus**. Erän tasaus on käytettävissä erätilauksissa, joiden tila on **Aloitettu**.

Erän tasausta voidaan yleensä käyttää erätilauksissa, jos reseptissä on ainakin yksi reseptirivi, jonka **ainesosatyyppi** on *Aktiivinen*. (Tämän säännön poikkeusta käsitellään jäljempänä tässä ohjeaiheessa kohdassa Erätilaukset, joissa ei voi käyttää erän tasausta.)

Erän tasausprosessi voidaan jakaa kahteen aliprosessiin:

1. Täsmäytä erän ainesosat
1. Vahvista ja vapauta resepti

### <a name="balance-batch-ingredients"></a>Täsmäytä erän ainesosat

Erän tasauksen ainesosat -aliprosessissa tuotantoerässä käytettyjen ainesosien määrä lasketaan valittujen vaikuttavia ainesosia sisältävien erien perusteella. Laskelma voidaan pääsääntöisesti suorittaa vain, jos kaikkia ainesosia on riittävästi. Et voi täsmäyttää vain osaa erästä, jonka erätilaus on määritetty tuottamaan.

> [!NOTE]
> Et voi tallentaa laskelmaa ja suorittaa sitten erän tasausprosessia myöhemmin. Jos suljet **Erän tasaus** -sivun, prosessin valmistumiseen tarvittava laskelma on toistettava.

### <a name="confirm-and-release-the-formula"></a>Vahvista ja vapauta resepti

Kun ainesosien määrät on laskettu, voit vahvistaa ja vapauttaa reseptin. Vapautusprosessi vaihtelee sen mukaan, onko varastonhallintaprosessit otettu käyttöön tuotteissa.

- Jos varastonhallintaprosessit on otettu käyttöön tuotteessa, reseptirivi vapautetaan varastoon varastonhallintaprosessien periaatteiden mukaan. Reseptirivi vapautetaan täsmäytettyä määriä vastaavina määrinä. Se vapautetaan erityiserille, jotka on valittu vaikuttavilla ainesosille.

    > [!NOTE]
    > Reseptirivit voidaan vapauttaa varastoon vain erän tasausprosessin osana. Vaikka tuotantomateriaalien vapauttamiseen varastoon on muita vaihtoehtoja, niitä ei voi käyttää reseptiriveillä.

- Jos varastonhallintaprosesseja ei ole otettu käyttöön tuotteessa, tuotteelle luodaan tuotannon keräysluettelo, kun vahvistat ja vapautat reseptin.

Voit yhdistää yhteen reseptiin tuotteet, joissa varastonhallintaprosessit on otettu käyttöön, ja tuotteet, joissa näin ei ole tehty. Kun yhdessä reseptissä kahden tyyppisiä tuotteita, tuotteet, joissa varastonhallintaprosessit on otettu käyttöön, vapautetaan varastoon. Tuotteille, joissa varastonhallintaprosesseja ei ole otettu käyttöön, luodaan keräysluettelo, kun resepti vahvistetaan ja vapautetaan.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Erätilaukset, joissa ei voi käyttää erän tasausta

On olemassa kaksi poikkeusta sääntöön, jonka mukaan erätilauksissa voi käyttää erän tasausta, jos reseptissä on ainakin yksi reseptirivi, jonka **ainesosatyyppi** on *Aktiivinen*.

1. Jos reseptissä on vaikuttava ainesosa tuotteelle, jossa varastonhallintaprosessit on otettu käyttöön mutta jonka eränumero on varaushierarkian sijainnin alapuolella, erätilauksessa ei voi käyttää erän tasausta.
1. Jos reseptin mittayksikkö ei ole sama kuin vaikuttavan ainesosan varastomittayksikkö, erän tasauta ei voi käyttää erätilauksessa.

Jos erätilauksessa ei voi käyttää erän tasausta, se käsitellään erätilausten tavallisen prosessisyklin mukaisesti.
