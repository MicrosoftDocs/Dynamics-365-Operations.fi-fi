---
title: Egyptin ALV-ilmoitus
description: Tässä artikkelissa kerrotaan, miten Egyptin ALV-palautuslomake konfiguroidaan ja muodostetaan.
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1d5788b2328a49f4725a6c689e29a7e784032fae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870032"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Egyptin ALV-ilmoitus (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten ALV-palautuslomake sekä myynti- ja ostokirjat määritetään ja luodaan yrityksille Egyptissä.

Egyptin ALV-palautuslomake on virallinen asiakirja, joka sisältää yhteenvedon tuloksena syntyvän arvonlisäveron erääntyvästä kokonaissummasta, syötetyn arvonlisäveron palautuksen kokonaissumman sekä näihin liittyvästä arvonlisäverosumman velasta. Lomaketta käytetään kaikille verovelvollisen tyypeille, ja se tulee täyttää manuaalisesti veroviranomaisen portaalin kautta. ALV-palautuslomaketta kutsutaan yleisesti ALV-palautusilmoitukseksi.

ALV-palautuslomake Dynamics 365 Financessa sisältää seuraavat raportit:

- ALV-palautuslomakkeen numero 10, joka sisältää erittelyn summista, oikaisuista ja rivinimikekohtaisista ALV-summista ALV-palautuslomakkeessa lainsäädännön mukaan.
- Myyntitapahtumien kirja
- Ostotapahtumien kirja

## <a name="prerequisites"></a>Edellytykset
Yrityksen ensisijainen osoite on on oltava Egyptissä.
Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraava ominaisuus:

   - (Egypti) Myynti- ja ostoveroraportin luokkahierarkia.

Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tuo **Sähköinen raportointi** -työtilassa seuraava sähköinen raportointimuoto tietovarastosta:

- ALV-ilmoitus, Excel (EG)

> [!NOTE]
> Edellä esitetty muoto perustuu **veroilmoituksen malliin** ja käyttää **veroilmoituksen mallimääritystä**. Lisäkonfiguraatiot tuodaan automaattisesti.

Lisätietoja sähköisen raportoinnin konfiguraatioiden tuomisesta on kohdassa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services  -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Sähköisen raportoinnin konfiguraatioiden lataaminen

Egyptin ALV-palautuslomakkeen toteutus, joka perustuu sähköisen raportoinnin konfiguraatioihin. Lisätietoja konfiguroitavan raportoinnin ominaisuuksista ja käsitteistä on kohdassa [Sähköinen raportointi](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tuotanto- ja käyttäjähyväksyntätestausympäristöille on tietoja kohdassa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Voit luoda ALV-palautuslomakkeen ja siihen liittyvät raportit egyptiläisessä yrityksessä lataamalla palvelimeen seuraavat konfiguraatiot:

- Veroilmoitus model.version.70.xml tai myöhempi versio
- Veroilmoituksen mallin mapping.version.70.120.xml tai myöhempi versio
- VAT-ilmoituksen Excel (EG).version.70.32 tai myöhempi versio

Kun olet ladanut ER-konfiguraatiot Lifecycle Services (LCS) -palvelusta tai yleisestä tietovarastosta, tee seuraavat toimet.

1. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.
1. Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda** > **Lataa XML-tiedostosta**.
1. Lataa tiedostot palvelimeen sen mukaan, missä järjestyksessä ne on lueteltu yllä. Kun kaikki konfiguraatiot on ladattu palvelimeen, konfiguraatiopuun pitäisi näkyä Financessa.

## <a name="set-up-application-specific-parameters"></a>Sovelluskohtaisten parametrien määrittäminen

Sovelluskohtaisien parametrien avulla voit määrittää kriteerit, joiden mukaan verotapahtumat luokitellaan ja lasketaan kullakin rivillä, kun raportti luodaan. Määritys perustuu nimikkeen arvonlisäveroryhmän, arvonlisäveroryhmän, arvonlisäverokoodin ja muiden hakumäärityksessä määritettyjen ehtojen konfiguraatioon.

Egyptin myynti- ja ostokirjaraportit sisältävät joukon sarakkeita, jotka vastaavat tiettyjä tapahtumaluokitteluja Egyptiä koskevina toiminto-, tuote- ja asiakirjatyyppeinä. Sen sijaan, että nämä uudet luokittelut sisällytettäisiin uuden viennin tietoina tapahtumien kirjaamisen yhteydessä, luokittelut määritetään kohdassa **Määritykset** > **Määritä sovelluskohtaiset parametrit** > **Määritys** esiteltyjen eri hakujen mukaan, jotta täytetään Egyptin ALV-raporttien vaatimukset. 

![Sovelluskohtaiset parametrit -sivu.](media/egypt-vat-declaration-setup1.png)

Näiden seuraavien hakukonfiguraatioiden avulla luokitellaan oston ja myynnin ALV-kirjojen raporttien tapahtumat:

- **PurchaseItemTypeLookup** > Sarake O: Nimiketyyppi
- **VATRateTypeLookup** > Sarake B: Verotyyppi
- **VATRateTypeLookup** > Sarake C: Taulukkonimiketyyppi
- **PurchaseOperationTypeLookup** > Sarake A: Asiakirjatyyppi
- **CustomerTypeLookup** > Sarake A: tiedostotyyppi
- **SalesOperationTypeLookup** > Sarake N: Toimintotyyppi
- **SalesItemTypeLookup** > Sarake O: Nimiketyyppi

Seuraavia ohjeita noudattamalla voit määrittää eri hakuja, joita käytetään ALV-ilmoituksen ja siihen liittyvien kirjojen raporttien luomisessa. 

1. Valitse **Sähköinen raportointi** -työtilassa **Määritykset** > **Määritys**, kun haluat määrittää säännöt, jotka yksilöivät verotapahtuman ALV-palautuslomakkeen liittyvässä ruudussa.
2. Valitse nykyinen versio ja valitse hakunimi **Haut**-pikavälilehdistä. Esimerkiksi **SalesItemTypeLookup**. Tämä haku yksilöi arvonlisäverokirjan luokitusten luettelon, jota veroviranomainen edellyttää.
3. Valitse **Ehdot**-pikavälilehdessä **Lisää** ja valitse uuden rivin **Hakutulos**-sarakkeessa liittyvä rivi, joka vastaa **sarakkeen O** luokittelua.
4. Valitse **Arvonlisäveroryhmä**-sarakkeesta arvonlisäveroryhmä, jota käytetään luokituksen tunnistamiseen. Esimerkiksi **Kotimaan myyntilasku**. Voit käyttää myös nimikkeen arvonlisäveroryhmää, verokoodia tai puumääritteiden yhdistelmää, jos konfiguraatio on määritetty muulla tavoin. 
5. Valitse **Nimi**-sarakkeesta verotapahtumaluokitus.
6. Toista vaiheet 3-5 kaikille käytettävissä oleville hauille.
7. Valitse **Lisää**, jos haluat sisällyttää lopullisen tietuerivin. Valitse **Hakutulos**-sarakkeesta **Ei sovellettavissa**. 
8. Valitse jäljellä olevissa sarakkeissa **Ei tyhjä**. 
9. Valitse **Tila**-kentässä **Valmis**.
10. Valitse **Tallenna** ja sulje sitten **Sovelluskohtaiset parametrit** -sivu.

> [!NOTE]
> Kun lisäät viimeisen tietueen (**Ei sovellettavissa**) määrität seuraavan säännön: Kun arvonlisäveroryhmä, nimikkeen arvonlisäveroryhmä, verokoodi ja nimi, jotka on välitetty argumentteina, eivät täytä aiempia sääntöjä, tapahtumia ei sisällytetä arvonlisäverokirjaan. Vaikka tätä sääntöä ei käytetä raportin luonnissa, sääntö auttaa välttämään raportin luonnissa virheitä, kun sääntömääritys puuttuu.

Seuraavat taulut ovat esimerkkejä kuvattujen hakukonfiguraatioiden ehdotetuista konfiguraatioista. 

**SalesItemTypeLookup**

| Haun tulos         | Linja | Arvonlisäveroryhmä    | Nimikkeen arvonlisäveroryhmä    | Verokoodi (koodi) | Nimi                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Kotimaa              | 1    | VAT_LOCAL          | *Ei tyhjä*             | *Ei tyhjä*     | Myynti                 |
| Kotimaa              | 2    | VAT_LOCAL          | *Ei tyhjä*             | *Ei tyhjä*     | SalesCreditNote       |
| Kotimaa              | 3    | VAT_FINALC         | *Ei tyhjä*             | *Ei tyhjä*     | Myynti                 |
| Kotimaa              | 4    | VAT_FINALC         | *Ei tyhjä*             | *Ei tyhjä*     | SalesCreditNote       |
| Kotimaa              | 5    | VAT_PUBLIO         | *Ei tyhjä*             | *Ei tyhjä*     | Myynti                 |
| Kotimaa              | 6    | VAT_PUBLIO         | *Ei tyhjä*             | *Ei tyhjä*     | SalesCreditNote       |
| Vie                | 7    | VAT_EXPORT         | *Ei tyhjä*             | *Ei tyhjä*     | Myynti                 |
| Vie                | 8    | VAT_EXPORT         | *Ei tyhjä*             | *Ei tyhjä*     | SalesCreditNote       |
| Kone ja välineistö | 9    | *Ei tyhjä*        | VAT_M&E                 | *Ei tyhjä*     | Myynti                 |
| Kone ja välineistö | 10   | *Ei tyhjä*        | VAT_M&E                 | *Ei tyhjä*     | SalesCreditNote       |
| Koneiden osat        | 11   | *Ei tyhjä*        | VAT_PARTS               | *Ei tyhjä*     | Myynti                 |
| Koneiden osat        | 12   | *Ei tyhjä*        | VAT_PARTS               | *Ei tyhjä*     | SalesCreditNote       |
| Vapautukset            | 13   | VAT_EXE            | *Ei tyhjä*           | *Ei tyhjä*     | SaleExempt            |
| Vapautukset            | 14   | VAT_EXE            | *Ei tyhjä*           | *Ei tyhjä*     | SalesExemptCreditNote |
| Ei käytettävissä        | 15   | *Tyhjä*            | *Tyhjä*                 | VAT_ADJ         | *Ei tyhjä*           |
| Ei käytettävissä        | 16   | *Ei tyhjä*        | *Ei tyhjä*             | *Ei tyhjä*     | *Ei tyhjä*           |

 **SalesOperationTypeLookup**

| Haun tulos  | Linja | Nimikkeen arvonlisäveroryhmä    | Alv-koodi    | Nimi                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Tavarat          | 1    | VAT_GOODS               | *Ei tyhjä* | Myynti                 |
| Tavarat          | 2    | VAT_GOODS               | *Ei tyhjä* | SalesCreditNote       |
| Tavarat          | 3    | VAT_GOODS               | *Ei tyhjä* | SaleExempt            |
| Tavarat          | 4    | VAT_GOODS               | *Ei tyhjä* | SalesExemptCreditNote |
| Palvelut       | 5    | VAT_SERV                | *Ei tyhjä* | Myynti                 |
| Palvelut       | 6    | VAT_SERV                | *Ei tyhjä* | SalesCreditNote       |
| Palvelut       | 7    | VAT_SERV                | *Ei tyhjä* | SaleExempt            |
| Palvelut       | 8    | VAT_SERV                | *Ei tyhjä* | SalesExemptCreditNote |
| Oikaisut    | 9    | *Tyhjä*                 | VAT_ADJ     | Myynti                 |
| Oikaisut    | 10   | *Tyhjä*                 | VAT_ADJ     | SalesCreditNote       |
| Ei käytettävissä | 11   | *Ei tyhjä*             | *Ei tyhjä* | *Ei tyhjä*           |

**PurchaseItemTypeLookup**

| Haun tulos          | Linja | Nimikkeen arvonlisäveroryhmä    | Alv-koodi    | Nimi                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Tavarat                  | 1    | VAT_GOODS               | *Ei tyhjä* | Osto                 |
| Tavarat                  | 2    | VAT_GOODS               | *Ei tyhjä* | PurchaseCreditNote       |
| Palvelut               | 3    | VAT_SERV                | *Ei tyhjä* | Osto                 |
| Palvelut               | 4    | VAT_SERV                | *Ei tyhjä* | PurchaseCreditNote       |
| Kone ja välineistö  | 5    | VAT_M&E                 | *Ei tyhjä* | Osto                 |
| Kone ja välineistö  | 6    | VAT_M&E                 | *Ei tyhjä* | PurchaseCreditNote       |
| Koneiden osat         | 7    | VAT_PARTS               | *Ei tyhjä* | Osto                 |
| Koneiden osat         | 8    | VAT_PARTS               | *Ei tyhjä* | PurchaseCreditNote       |
| Vapautukset             | 9    | VAT_EXE                 | *Ei pankkia*  | PurchaseExempt           |
| Vapautukset             | 10   | VAT_EXE                 | *Ei tyhjä* | PurchaseExemptCreditNote |
| Ei käytettävissä         | 11   | *Ei tyhjä*             | *Ei tyhjä* | *Ei tyhjä*              |

**PurchaseOperationTypeLookup**

| Haun tulos  | Linja | Arvonlisäveroryhmä  | Alv-koodi    | Nimi                     |
|----------------|------|------------------|-------------|--------------------------|
| Kotimaa       | 1    | VAT_LOCAL        | *Ei tyhjä* | Osto                 |
| Kotimaa       | 2    | VAT_LOCAL        | *Ei tyhjä* | PurchaseCreditNote       |
| Kotimaa       | 3    | VAT_LOCAL        | *Ei tyhjä* | PurchaseExempt           |
| Kotimaa       | 4    | VAT_LOCAL        | *Ei tyhjä* | PurchaseExemptCreditNote |
| Tuotu       | 5    | VAT_IMPORT       | *Ei tyhjä* | Osto                 |
| Tuotu       | 6    | VAT_IMPORT       | *Ei tyhjä* | PurchaseCreditNote       |
| Tuotu       | 7    | VAT_IMPORT       | *Ei tyhjä* | PurchaseExempt           |
| Tuotu       | 8    | VAT_IMPORT       | *Ei tyhjä* | PurchaseExemptCreditNote |
| Oikaisut    | 9    | *Tyhjä*          | VAT_ADJ     | PurchaseCreditNote       |
| Oikaisut    | 10   | *Tyhjä*          | VAT_ADJ     | Osto                 |
| Ei käytettävissä | 11   | *Ei tyhjä*      | *Ei tyhjä* | *Ei tyhjä*              |

**CustomerTypeLookup**

|    Haun tulos    | Linja | Arvonlisäveroryhmä |
|---------------------|------|-----------------|
| Organisaatio        |  1   | VAT_LOCAL       |
| Organisaatio        |  2   | VAT_EXPORT      |
| Organisaatio        |  3   | VAT_EXE         |
| Loppukuluttaja      |  4   | VAT_FINALC      |
| Julkinen organisaatio |  5   | VAT_PUBLIO      |
| Ei käytettävissä      |  6   | *Ei tyhjä*     |

**VATRateTypeLookup**

| Haun tulos  | Linja | Verokoodi (koodi) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Ei tyhjä*     |
| SecondTable    | 4    | *Ei tyhjä*     |
| Ei käytettävissä | 5    | *Ei tyhjä*     |


## <a name="set-up-general-ledger-parameters"></a>Kirjanpidon parametrien määrittäminen

Voit luoda ALV-palautuslomakkeen raportin Microsoft Excel -muodossa, kun määrität ER-muodon **Kirjanpitoparametrit**-sivulla.

1. Siirry kohtaan **Vero** > **Asetukset** > **Kirjanpitoparametrit**.
2. Valitse **Arvonlisävero**-välilehden **Veroasetukset**-osan **ALV-ilmoituksen muodon määritys** -kentästä **ALV-ilmoituksen Excel (EG)**. Jos jätät tämän kentän tyhjäksi, arvonlisäveron vakioraportti luodaan SSRS-muodossa.
3. Valitse **Luokkahierarkia**. Tämän luokan avulla Ulkomaankauppa-välilehden tapahtumien kauppatavarakoodin avulla käyttäjät voivat valita ja luokitella tavaroita ja palveluja. Tämän luokituksen kuvaus on eritelty myynti- ja ostotapahtumaraporteissa. Tämä määritys on valinnainen.

![Ilmoituslomake.](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Luo ALV-palautusraportti
Kauden ALV-palautusraportin valmistelu- ja lähetysprosessi perustuu arvonlisäveron maksutapahtumiin, jotka on kirjattu Tilitä ja kirjaa arvonlisävero -työn suorituksen aikana. Lisätietoja arvonlisäveron tilityksestä ja raportoinnista on kohdassa [Arvonlisäveron yleiskatsaus](../general-ledger/indirect-taxes-overview.md).

Luo veroilmoitusraportti noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Vero** > **ilmoitukset** > **Arvonlisävero** > **Ilmoita arvonlisävero tilityskaudelle** tai **Tilitä ja kirjaa arvonlisävero**.
2. Valitse **Tilityskausi**.
3. Valitse alkamispäivämäärä ja valitse sitten arvonlisäveron maksun versio.
5. Valitse **OK**. 
6. Kirjoita tarvittaessa edellisen kauden hyvityssumma tai jätä summa nollaksi.
7. Valitse **Raportin tiedot** -kentästä jokin seuraavista vaihtoehdoista. 
   - **Ostojen ALV-kirja**: Luo ostoverotapahtumien erittelyraportti.
   - **Myynnin ALV-kirja**: Luo myyntiverotapahtumien erittelyraportti.
   - **ALV-ilmoitus**: Luo vain ALV-ilmoituksen palautuslomake.
8. Kirjoita lomakkeen määritystä varten rekisteröidyn henkilön nimi.
9. Valitse kieli. Kaikki raportit käänetään kielille **en-us** ja **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


