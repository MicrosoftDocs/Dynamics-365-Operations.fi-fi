---
title: ALV-ilmoitus (Saksa)
description: Tässä artikkelissa kuvataan, miten ALV-ilmoitus määritetään ja luodaan Saksassa ennakkoon virallisessa XML-muodossa.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 04c625b554d96f8ed28ceffef9647fe9cbf7fe2f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689457"
---
# <a name="vat-declaration-germany"></a>ALV-ilmoitus (Saksa)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten ALV-ilmoitus määritetään ja luodaan Saksassa ennakkoon virallisessa XML-muodossa. Tässä artikkelissa kerrotaan myös, miten ALV-ilmoitus esikatsellaan Microsoft Excelissä.

Voit luoda raportin automaattisesti luomalla tarpeeksi arvonlisäverokoodeja, jotta voit pitää erillisen ALV-kirjanpidon kutakin ennakko-ALV-ilmoituksen ruutua varten. Lisäksi ALV-ennakonpidätysilmoituksen sähköisen raportoinnin (ER) sovelluskohtaisten parametrien avulla arvonlisäverokoodit liitetään ALV-ilmoituksen ruutujen valintojen hakutuloksiin.

Saksaa varten on määritettävä **Raporttikentän haku**. Lisätietoja sovelluskohtaisten parametrien määrittämisestä on jäljempänä tässä artikkelissa [ALV-ilmoituskenttien sovelluskohtaisten parametrien määrittäminen](#set-up-application-specific-parameters-for-vat-declaration-fields) -osassa.

Seuraavassa taulukossa Hakutulos-sarakkeessa näkyy hakutulos, joka on määritetty valmiiksi tietylle ALV-ilmoitusriville ALV-ilmoitusmuodossa. Näiden tietojen avulla voit liittää arvonlisäverokoodit oikein hakutuloksiin ja sitten ALV-ilmoituksen riviin.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>ALV-ilmoituksen yleiskuvaus

Saksan ALV-ennakkoilmoitus sisältää seuraavat tiedot.

**OSA – TOIMITUKSET JA MUUT PALVELUT**

**Verollinen myynti**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                                                                                                                      | Haun tulos                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Ilman koodia     | Verollinen myynti veroprosentilla 19.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – miinusmerkillä             |
| 21  | 86             | Ilman koodia     | Verollinen myynti veroprosentilla 7.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – miinusmerkillä               |
| 22  | 35             | 36               | Verollinen myynti muilla veroprosenteilla.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – miinusmerkillä      |
| 23  | 77             | *Ei verosummaa*  | Toimitukset maanviljelys- ja metsätalousyrityksiltä Saksan ALV-lain (UStG) §24 mukaan asiakkaille, joilla on ALV-tunnus. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – miinusmerkillä |
| 24  | 76             | 80               | Myynti, josta veroa on maksettava UStG §24 mukaan (sahatuotteet, juomat ja alkoholinesteet).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Verovapaa myynti tuloveron vähennyksellä**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                                                       | Haun tulos                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Ei verosummaa*  | EU:n sisäiset toimitukset asiakkaille, joilla on ALV-tunnus.                       | 26-EUSales                          |
| 27  | 44             | *Ei verosummaa*  | Uusien ajoneuvojen EU:n sisäiset toimitukset ostajille, joilla ei ole ALV-tunnusta.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Ei verosummaa*  | Uusien ajoneuvojen EU:n sisäiset toimitukset yrityksen ulkopuolella.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Ei verosummaa*  | Muut verovapaat myynnit, joista on vähennetty ostovero, esimerkiksi vientitoimitukset. | 29-ExportOtherTaxFreeSales          |

**Verovapaa myynti ilman tuloveron vähennystä**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                            | Haun tulos                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Ei verosummaa*  | Veroton myynti, jossa ei ole ostoverovähennystä. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**EU:n sisäiset hankinnat**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                                                                                                   | Haun tulos                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Ei verosummaa*  | Veroton EU:n sisäinen hankinta, joka sisältää joitakin kohteita ja sijoituskultaa.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Ilman koodia     | Verotettavat EU:n sisäiset hankinnat veroprosentilla 19.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Ilman koodia     | Verotettavat EU:n sisäiset hankinnat veroprosentilla 7.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Verotettavat EU:n sisäiset hankinnat muilla veroprosenteilla.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Uusien ajoneuvojen verotettavat EU:n sisäiset hankinnat toimittajilta, joilla ei ole ALV-tunnusta, yleisellä veroprosentilla. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**OSA – EDUNSAAJA VERON PERIJÄNÄ**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                                                        | Haun tulos                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Muut muut yhteisön alueeseen perustuvat palvelut yrittäjänä.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Myynti, joka kuuluu UStG:n osan 13b (2) nron 3 alle.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Muuta palvelut, jotka kuuluvat UStG:n osan 13b (2) nron 1, 2 ja 4-12 alle. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**OSA – MYYNTIÄ KOSKEVAT LISÄTIEDOT**

| Rivi | Ruutu – veron peruste  | Ruutu - verosumma. | Kuvaus                                                                                                | Haun tulos                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Ei verosummaa*  | Ensimmäisen asiakkaan toimitukset yhteisön sisäisissä kolmikantatapahtumissa.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Ei verosummaa*  | Sen suorittaneen yrittäjän verollinen myynti, jolle palvelun vastaanottaja on velkaa veron. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Ei verosummaa*  | Muut ei-verotettavat palvelut.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Ei verosummaa*  | Muu veroton myynti, kun suorituspaikka ei ole Saksassa.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Ei verosummaa* | *Ei verosummaa*  | ALV.                                                                                                       | Rivi 20 + Rivi 21 + Rivi 22 + Rivi2 4 + Rivi 34 + Rivi 35 + Rivi 36 + Rivi 37 + Rivi 40 + Rivi 41 + Rivi 42 |

**OSA – VÄHENNYSKELPOINEN OSTOVERO**

| Rivi | Ruutu - verosumma. | Kuvaus                                                                                                | Haun tulos                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Muiden yritysten, palveluiden ja yhteisön sisäisten kolmikantatapahtumien ostolaskun veron summat.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – miinusmerkillä                                                                   |
| 56  | 61               | Tuloverosummat yhteisön sisäisestä tuotteiden hankinnasta.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Toteutuneet tuonnin arvonlisäverot.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | UStG:n kohdassa §13b tarkoitettujen palvelujen ostoverosummat.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Ostoverosummat, jotka lasketaan yleisten keskimääräisten verojen mukaisesti.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – miinusmerkillä                                                                                    |
| 60  | 59               | Uusien ajoneuvojen ostoveron vähennykset yhteisön sisäisissä toimituksissa yrityksen ja pienyritysten ulkopuolella. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – miinusmerkillä                                                                  |
| 61  | 64               | Ostoverovähennyksen oikaisu.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Jäljellä oleva summa.                                                                                      | Rivi 52 – Rivi 55 – Rivi 56 – Rivi 57 – Rivi 58 – Rivi 50 – Rivi 60 – Rivi 61                                                                                                        |

**OSA – MUUT VEROSUMMAT**

| Rivi | Ruutu - verosumma. | Kuvaus                                                                                                                                                                                                                                                         | Haun tulos                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Vero, joka johtuu verotusmuodon muutoksesta ja maksuverojen lisäveroista sen vuoksi, että veroprosentti on muuttunut.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Virheelliset tai perusteettomat verosummat, jotka näkyvät laskuissa, ja verosummat, jotka organisaatio on velkaa UStG:n osion 6a (4) lausekkeen 2, osan 17 (1) lausekkeen 7 tai osan 25b (2) mukaisesti, tai jotka alihankintayritys tai varaston ylläpitäjä on velkaa. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Kiinteän erityisennakkomaksun vähennys pysyvää pidennystä varten. Tämä rivi täytetään yleensä vain verokauden viimeisen ennakkoilmoituksen yhteydessä.                                                                                                  | Käyttäjän syöteparametri raportin valintaikkunassa |
| 68  | 83               | Jäljellä oleva arvonlisäveron ennakkomaksu ja jäljelle jäävä ylijäämä. Sisällytä miinusmerkki summan eteen.                                                                                                                                                          | Rivi 62 + Rivi 64 – Rivi 65 – Rivi 66             |

**OSA – VÄHENNYKSIÄ KOSKEVAT LISÄTIEDOT**

| Rivi | Ruutu – veron peruste | Ruutu - verosumma. | Kuvaus                                                            | Haun tulos                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Rivien 20-24 veroperusteen vähentäminen.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Rivien 55, 59 ja 60 vähennettävien ostoverosummien vähennys. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Oston käänteinen verovelvollisuus

Jos määrität arvonlisäverokoodit kirjaamaan saapuvan käänteisen arvonlisäveron käyttämällä käyttöveroa, liitä arvonlisäverokoodit "UseTax"-merkkijonon sisältävän **Raporttikentän haku** -nimen hakutuloksiin.

Vaihtoehtoisesti voit konfiguroida kaksi erillistä arvonlisäverokoodia: toisen erääntyville arvonlisäveroille ja toisen ALV-vähennykselle. Liitä sitten kukin koodi vastaaviin **Raporttikentän haku** -hakutuloksiin.

Voit esimerkiksi määrittää vakiohintaisia verotettavia yhteisön sisäisiä hankintoja varten arvonlisäverokoodin **UT_S_EU** käyttöveron avulla ja liittää sen **Raporttikentän haku** -hakutulosten **34-UseTaxEUPurchaseStandard**-hakutulokseen. Tällöin arvonlisäverokoodin **UT_S_EU** summat näkyvät ruuduissa 089 ja 061 (rivit 34 ja 56).

Vaihtoehtoisesti voit määrittää kaksi arvonlisäverokoodia:

  - **VAT_S_EU**, jonka veroprosenttiarvo on -19 prosenttia.
  - **InVAT_S_EU**, jonka veroprosenttiarvo on 19 prosenttia.

Liitä sitten koodit vastaaviin **Raporttikentän haku** -hakutuloksiin seuraavasti:

  - Liitä **VAT_S_EU** **34-EUPurchaseStandard**-hakutulokseen.
  - Liitä **InVAT_S_EU** **56-InputTaxEUPurchase**-hakutulokseen.

Tällöin arvonlisäverokoodin **VAT_S_EU** summat näkyvät ruudussa 089 (rivi 34). Arvonlisäverokoodin **InVAT_S_EU** summat näkyvät ruudussa 061 (rivi 56).

Lisätietoja käänteisen verovelvollisuuden määrittämisestä: [Käänteinen verovelvollisuus](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfiguroi järjestelmäparametrit

ALV-ilmoituksen muodostamiseksi sinun on määritettävä organisaation veronumero (Steuernummer).

1. Valitse **Organisaation hallinto** > **Organisaatiot** > **Yritykset**.
2. Valitse yritys ja sitten **Rekisteröintitunnukset**.
3. Valitse tai luo osoite Saksassa. Valitse sitten **Rekisteröintitunnus**-pikavälilehdessä **Lisää**.
4. Valitse **Rekisteröintityyppi**-kentässä Saksaa varten rekisteröity rekisteröintityyppi, joka käyttää **Yritystunnus (COID)** -rekisteröintiluokkaa.
5. Anna **Rekisteröintinumero**-kentässä veronumero.
6. Kirjoita **Voimassa**-kenttään **Yleiset**-välilehdessä päivämäärä, jolloin numero tulee voimaan.

Lisätietoja rekisteröintiluokkien ja rekisteröintityyppien määrittämisestä on kohdassa [Rekisteröintitunnukset](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Saksan ALV-ilmoituksen määritys

### <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen

Avaa **Sähköisen raportoinnin** työtila ja tuo seuraavat versiot tai myöhemmät versiot seuraavista ER-muodoista:

   - VAT Declaration Excel (DE).version.101.16.12.xml
   - VAT Declaration XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Sovelluskohtaisten parametrien määrittäminen ALV-ilmoituskentille

Kun haluat luoda ALV-ilmoituksen automaattisesti, liitä arvonlisäverokoodit sovellukseen ja hakutuloksiin ER-konfiguraatiossa.

> [!NOTE]
> Suosittelemme, että otat tätä varten käyttöön **Käytä sovelluskohtaisia parametreja sähköisen raportoinnin muotojen aiemmista versioista** -ominaisuuden **Ominaisuuksienhallinta**-työtilassa. Kun tämä ominaisuus on käytössä, ER-muodon aiemmassa versiossa konfiguroivat parametrit tulevat automaattisesti käyttöön saman muodon myöhemmässä versiossa. Jos tätä toimintoa ei ole otettu käyttöön, sovelluskohtaiset parametrit on määritettävä erikseen kullekin muotoversiolle. **Käytä sovelluskohtaisia parametreja aiemmista ER-muotojen versioista** -ominaisuus on käytettävissä **Ominaisuuksien hallinta** -työtilassa Financen versiosta 10.0.23 alkaen. Lisätietoja ER-muodon parametrien määrittämisestä kullekin yritykselle on kohdassa [ER-muodon parametrien määrittämisestä kullekin yritykselle](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Seuraavia ohjeita noudattamalla voit määrittää, mitkä arvonlisäverokoodit luovat mitkä ALV-ilmoituksen ruudut.

1. Valitse **Työtilat** > **Sähköinen raportointi** >**Raportointimääritykset**.
2. Valitse **VAT declaration XML (DE)** -konfiguraatio ja valitse sitten **Määritykset \> Sovelluskohtaisten parametrien määritys**.
3. Valitse **Sovelluskohtaiset parametrit** -sivun **Haku**-pikavälilehdestä **Raporttikentän haku**.
4. Liitä arvonlisäverokoodit ja raporttikentät määrittämällä seuraavat **Ehdot**-pikavälilehden kentät.

    | Kenttä                  | Kuvaus                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Haun tulos          | Valitse raporttikentän arvo. Lisätietoja arvoista ja niiden määrityksestä ALV-ilmoitusriveille on tämän artikkelin aiemmassa [ALV-ilmoituksen yhteenveto](#vat-declaration-overview) -osassa.                                                                                               |
    | Alv-koodi               | Valitse raporttikenttään liitettävä arvonlisäverokoodi. Valittua arvonlisäverokoodia käyttävät kirjatut verotapahtumat kerätään soveltuvassa ilmoitusruudussa. On suositeltavaa erotella arvonlisäverokoodit siten, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun. |
    | Tapahtumaluokan valitsin | Jos olet luonut tarpeeksi arvonlisäverokoodeja ilmoitusruudun määrittämiseksi, valitse **\*Ei tyhjä\***. Jos et luonut tarpeeksi arvonlisäverokoodeja niin, että yksi arvonlisäverokoodi luo summia vain yhteen ilmoitusruutuun, voit määrittää tapahtumaluokan valitsimen. Seuraavat tapahtumaluokan valitsimet ovat käytettävissä:</br>-   **Osto**</br>-   **PurchaseExempt** (verovapaa osto)</br>-   **PurchaseReverseCharge** (oston käänteisen kulun verosaatavat)</br>-   **Myynti**</br>-   **SalesExempt** (veroton myynti)</br>-   **SalesReverseCharge** (oston käänteisen kulun tai myynnin käänteisen kulun maksettava vero)</br>-   **Käyttövero**. </br>Lisäksi kutakin tapahtumaluokan valitsinta varten on käytettävissä hyvityslaskun luokan valitsin. Yksi näistä luokan valitsimista on esimerkiksi **PurchaseCreditNote** (ostohyvityslasku).</br>Luo jokaiselle arvonlisäverokoodille kaksi riviä: yksi, jolla on tapahtumaluokan valitsimen arvo ja toinen, jolla on tapahtumaluokan valitsin hyvityslaskun arvoa varten. |

    > [!NOTE]
    > Liitä kaikki arvonlisäverokoodit hakutuloksiin. Jos jokin arvonlisäverokoodi ei saa luoda arvoja ALV-ilmoitukseen, liitä ne **Muut**-hakutulokseen.

    ![Sovelluskohtaiset parametrit -sivu](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Muuta **Tila**-kentän arvoksi **Valmis**.
6. Valitse toimintoruudusta **Vie**, kun haluat viedä sovelluskohtaisten parametrien asetukset.
7. Valitse **VAT declaration Excel (DE)** -konfigurointi ja tuo **VAT declaration Excel (DE)** -kohteen parametrit valitsemalla toimintoruudusta **Tuo**.
8. Valitse **Tila**-kentässä **Valmis**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>ALV-raportointimuodon asetus Excelin esikatselua varten

1. **ALV-ilmoitusmuodon raportit**-ominaisuus on etsittävä ja otettava käyttöön **Ominaisuuksien hallinta** -työtilassa.
2. Valitse **Kirjanpito** >  **Kirjanpidon asetukset** >  **Kirjanpitoparametrit**.
3. Valitse **Arvonlisävero**-välilehden **Veroasetukset**-pikavälilehden **ALV-ilmoituksen muodon määritys** -kentästä **VAT declaration Excel (DE)**.

   Tämä muoto tulostetaan, kun suoritat **Ilmoita arvonlisävero tilityskaudelle** -raportin. Se tulostetaan myös, kun valitset **Arvonlisäveromaksut**-sivulla **Tulosta**.

4. Jos korjaukset on raportoitava, määritä **Erityisraportti**-osan **Sisällytä korjaukset** -kohdan arvoksi **Kyllä**.
5. Valitse **Veroviranomaiset**-sivulla veroviranomainen ja valitse sitten **Raportin asettelu** -kentästä **Oletus**.

Jos konfiguroit ALV-ilmoituksen yrityksessä, jossa on [useita ALV-rekisteröintejä](emea-reporting-for-multiple-vat-registrations.md), toimi seuraavasti:

1. Valitse **Kirjanpito** >  **Kirjanpidon asetukset** >  **Kirjanpitoparametrit**.
2. Valitse **Arvonlisävero**-välilehden **Sähköisen raportoinnin maat/alueet** -pikavälilehdessä **DEU**-rivillä ER-muoto **VAT Declaration Excel (DE)**.

## <a name="set-up-electronic-messages"></a>Sähköisten sanomien määrittäminen

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Lataa ja tuo tietopaketti, joka sisältää sähköisten viestien esimerkkiasetukset

Tietopaketti sisältää sähköisen sanoman asetuksia, joita käytetään ALV-ilmoituksen luomiseen XML-muodossa ja sen esikatselemiseen Excelissä. Voit laajentaa näitä asetuksia tai luoda omia. Lisätietoja sähköisten viestien käytöstä ja omien asetusten luomisesta on kohdassa [Sähköiset viestit](../general-ledger/electronic-messaging.md).

1. Valitse [Microsoft Dynamics Lifecycle Services(LCS)](https://lcs.dynamics.com/v2) -kohdan jaetussa käyttöomaisuuskirjastossa käyttöomaisuuserän tyypiksi **Tietopaketti** ja lataa sitten **DE – ALV-ilmoitus – EM** -paketti. Ladatun tiedoston nimi on **DE VAT declaration EM package.zip**.
2. Valitse Dynamics 365 Financessa **Tietojen hallinta** -työtilassa **Tuo**.
3. Kirjoita **Tuo**-pikavälilehden **Ryhmän nimi**-kenttään työn nimi.
4. Valitse **Valitut yksiköt** -välilehdessä **Lisää tiedosto**.
5. Varmista **Lisää tiedosto** -valintaikkunassa, että **Lähteen tietomuoto** -kentän arvo on **Paketti**, valitse **Lataa palvelimeen ja lisää** sekä valitse sitten aiemmin lataamasi zip-tiedosto.
6. Valitse **Sulje**.
7. Valitse tietoyksiköiden lataamisen jälkeen toimintoruudusta **Tuo**.
8. Siirry kohtaan **Vero** > **Kyselyt ja raportit** > **Sähköiset sanomat** > **Sähköiset sanomat** ja vahvista tuodun sähköisen sanoman käsittely.

### <a name="configure-electronic-messages"></a>Sähköiset sanomat – määritys

1. Valitse **Vero** > **Asetukset** > **Sähköiset sanomat** > **Tietueiden täyttötoiminnot**.
2. Valitse **DE – Täytä ALV-palautustietueet** -rivi ja valitse **Muokkaa kyselyä**.
3. Suodatinta käyttämällä voit määrittää raporttiin sisällytettävät tilityskaudet.
4. Jos haluat raportoida muiden tilityskausien verotapahtumat eri ilmoituksessa, luo uusi **Täytä tietueet** -toimenpide ja valitse asianmukaiset tilityskaudet.

## <a name="preview-the-vat-declaration-in-excel"></a>ALV-ilmoituksen esikatselu Excelissä

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>ALV-ilmoituksen esikatselu Excelissä kausittaisen Ilmoita arvonlisävero tilityskaudelle -tehtävän avulla

1. Valitse **Vero** > **Kausittaiset tehtävät** > **Ilmoitukset** > **Arvonlisävero** > **Ilmoita arvonlisävero tilityskaudelle**.
2. Valitse arvo **Tilityskausi**-kentässä.
3. Valitse **Arvonlisäveron maksuversio** -kentässä jokin seuraavista arvoista:

    - **Alkuperäinen**: Luo raportti alkuperäisen arvonlisäveromaksun arvonlisäverotapahtumista tai ennen arvonlisäveromaksun muodostamista.
    - **Oikaisut**: Luo raportti kaikkien seuraavien arvonlisäveromaksujen arvonlisäverotapahtumista kaudella.
    - **Koko luettelo**: Luo raportti kaikista arvonlisäverotapahtumista kaudella, sisältäen alkuperäiset ja korjaukset.

4. Valitse raportointikauden aloituspäivämäärä **Aloituspäivämäärä**-kentästä.
5. Valitse **OK** ja tarkista Excel-raportti.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Tilitä ja kirjaa arvonlisävero

1. Valitse **Vero** > **Kausittaiset tehtävät** > **Ilmoitukset** > **Arvonlisävero** > **Tilitä ja kirjaa arvonlisävero**.
2. Valitse arvo **Tilityskausi**-kentässä.
3. Valitse **Arvonlisäveron maksuversio** -kentässä jokin seuraavista arvoista:

    - **Alkuperäinen**: Luo alkuperäinen arvonlisäveromaksu tilityskaudelle.
    - **Viimeisimmät korjaukset**: Luo oikaisun arvonlisäveromaksu sen jälkeen, kun alkuperäinen tilityskauden arvonlisäveromaksu on luotu.

4. Valitse raportointikauden aloituspäivämäärä **Aloituspäivämäärä**-kentästä.
5. Valitse **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>ALV-ilmoituksen esikatselu Excelissä arvonlisäveromaksusta

1. Siirry kohtaan **Vero** > **Kyselyt ja raportit** > **Arvonlisäverokyselyt** > **Arvonlisäveromaksut** ja valitse arvonlisäveron maksurivi.
2. Valitse ensin **Tulosta raportti** ja sitten **OK**.
3. Tarkista valitulle arvonlisäveron maksuriville luotu Excel-tiedosto.

    > [!NOTE]
    > Raportti luodaan vain valitulle arvonlisäveron maksuriville. Jos haluat luoda esimerkiksi korjausilmoituksen, joka sisältää kauden kaikki korjaukset, tai korvaavan ilmoituksen, joka sisältää alkuperäiset tiedot ja kaikki korjaukset, käytä kausittaista tehtävää **Ilmoita arvonlisävero tilityskaudelle**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>ALV-ilmoituksen muodostaminen sähköisistä sanomista

Kun muodostat raportin sähköisten viestien avulla, voit kerätä verotietoja useista yrityksistä. Lisätietoja on tässä artikkelissa jäljempänä [ALV-ilmoituksen suorittaminen useille yrityksille](#run-a-vat-declaration-for-multiple-legal-entities) -osassa.

Seuraavat vaiheet koskevat sähköisen sanoman käsittelyesimerkkiä, jonka olet tuonut LCS:n jaetusta käyttöomaisuuskirjastosta.

1. Valitse **Vero** > **Kyselyt ja raportit** > **Sähköiset sanomat** > **Sähköiset sanomat**.
2. Valitse vasemmasta ruudusta **DE – ALV-ilmoitus**.
3. Valitse **Sanomat**-pikavälilehdessä **Uusi** ja valitse sitten **Suorita käsittely** -valintaikkunassa **OK**.
4. Valitse luotava sanomarivi, kirjoita kuvaus ja määritä sitten ilmoituksen alkamis- ja päättymispäivät.

    > [!NOTE]
    > Vaiheet 5-7 ovat valinnaisia.

5. Valinnainen: Valitse **Sanomat**-pikavälilehdessä **Kerää tiedot** ja valitse sitten **OK**. Aiemmin luodut arvonlisäveromaksut lisätään sanomaan. Lisätietoja on tämän artikkelin aiemmassa [Tilitä ja kirjaa arvonlisävero](#settle-and-post-sales-tax) -osassa. Jos ohitat tämän vaiheen, voit silti luoda ALV-ilmoituksen käyttämällä **Veroilmoituksen versio** -kenttää **Ilmoitus**-valintaikkunassa.
6. Valinnainen: Tarkista **Sanomanimikkeet**-pikavälilehdessä käsittelyyn siirretyt arvonlisäveromaksut. Oletusarvon mukaan kaikki valitun kauden arvonlisäveromaksut, jotka eivät sisälly saman käsittelyn muihin sanomaan, sisällytetään mukaan.
7. Valinnainen: Tarkista arvonlisäveromaksut valitsemalla **Alkuperäinen tiedosto**. Voit myös sulkea arvonlisäveromaksut pois käsittelystä valitsemalla **Poista**. Jos ohitat tämän vaiheen, voit silti luoda ALV-ilmoituksen käyttämällä **Veroilmoituksen versio** -kenttää **Ilmoitus**-valintaikkunassa.
8. Valitse **Sanomat**-pikavälilehdessä **Päivitä tila**. Valitse **Päivitä tila** -valintaikkunassa **Valmis luotavaksi** ja valitse sitten **OK**. Vahvista, että sanoman tilaksi tulee **Valmis luotavaksi**.
9. Valitse **Luo raportti**. Voit esikatsella ALV-ilmoituksen summia valitsemalla **Suorita käsittely** -valintaikkunassa **Esikatsele raporttia** ja valitsemalla sitten **OK**.
10. Määritä **Sähköisen raportoinnin parametrit** -valintaikkunassa seuraavat kentät ja valitse **OK**.

    | **Kenttä**                                   | **Kuvaus**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Tilityskausi                           | Valitse tilityskausi. Jos valitsit **Kerää tiedot** vaiheessa 5, voit jättää tämän kentän tyhjäksi. Raportti luodaan arvonlisäverotapahtumista, jotka sisältyvät kerättyihin arvonlisäveromaksuihin. |
    | Veroilmoituksen versio                     | Valitse jokin seuraavista:</br>-   **Alkuperäinen** – Luo raportti alkuperäisen arvonlisäveromaksun arvonlisäverotapahtumista tai ennen arvonlisäveromaksun muodostamista.</br>-   **Oikaisut** – Luo raportti kaikkien seuraavien arvonlisäveromaksujen arvonlisäverotapahtumista kaudella.</br>-   **Koko luettelo** – Luo raportti kaikista arvonlisäverotapahtumista kaudella, sisältäen alkuperäiset ja korjaukset.|
    | Verollinen edustaja | Valitse tarvittaessa osapuoli, joka on ALV-ilmoituksen veroedustaja. Valitun osapuolen tiedot viedään **DatenLieferant**-nimiseen XML -elementtiin. |
    | Yhteyshenkilö | Valitse organisaation henkilö, joka on tiedon toimittaja. Valitun henkilön tiedot viedään **DatenLieferant**-nimiseen XML -elementtiin. |
    | Korjaava palautus | Valitse **Kyllä**, jos tämä on korjaava ALV-ilmoitus. Tässä tapauksessa XML-elementin KZ10 arvo on **1**.|
    | Tukevat asiakirjat | Valitse **Kyllä**, jos lähetät myös lisäasiakirjoja. Tässä tapauksessa XML-elementin KZ22 arvo on **1**.|
    | SEPA (Single Euro Payments Area) -suoraveloitusvaltakirja peruutetaan poikkeuksena| Valitse **Kyllä**, jos SEPA-suoraveloituksen toimeksianto peruutetaan poikkeuksena tälle rekisteröintiä edeltävälle kaudelle. Esimerkiksi vastakirjauspyyntöjen vuoksi. Mahdollinen jäljelle jäävä saldo on maksettava erikseen. Tässä tapauksessa XML-elementin KZ26 arvo on **1**. |
    | Halutun hyvityssumman vastakirjaus | Valitse **Kyllä**, jos hyvityssumman vastakirjaus halutaan tai hyvityssumma on määritetty. Tässä tapauksessa XML-elementin KZ29 arvo on **1**. |
    | Erityisennakkomaksun pysyvä pidennys | Anna vähennyssumma kiinteän erityisennakkomaksun vähennys pysyvää pidennystä varten. Tämä vähennyssumma suoritetaan yleensä vain verokauden viimeisen ennakkorekisteröinnin yhteydessä. Summa viedään ALV-ilmoituksen riville 67 (ruutu 39) ja XML-elementille KZ39. |

11. Valitse sivun oikeasta yläkulmasta **Liitteet** ja valitse sitten **Avaa**.
12. Tarkista Excel-tiedoston summat ja valitse sitten **Luo raportti**.
13. Voit luoda ALV-ilmoituksen XML-muodossa valitsemalla **Suorita käsittely** -valintaikkunassa **Luo raportti** ja valitsemalla sitten **OK**.
14. Määritä **Sähköisen raportoinnin parametrit** -valintaikkunassa kentät vaiheessa 10 kuvatulla tavalla.
15. Valitse sivun oikeasta yläkulmasta **Liitteet**, lataa tiedosto ja käytä sitä lähetyksessä veroviranomaiselle.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>ALV-ilmoituksen suorittaminen useille yrityksille

Jos haluat käyttää muotoja yritysryhmän ALV-ilmoituksen raportoimiseen, sinun on ensin määritettävä kaikkien tarvittavien yritysten ER-muotojen sovelluskohtaiset parametrit arvonlisäverokoodeille.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Sähköisten viestien tietojen kerääminen usealta yritykseltä

Noudattamalla näitä ohjeita voit määrittää sähköiset sanomat, jotka keräävät tietoja useilta yrityksiltä.

1. Valitse **Työtilat** > **Ominaisuuden hallinta**.
2. Etsi ja valitse **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -toiminto luettelosta ja sitten **Ota käyttöön nyt**.
3. Valitse **Vero** > **Asetukset** > **Sähköiset sanomat \> Tietueiden täyttötoiminnot**.
4. Valitse **Tietueiden täyttötoiminto** -sivulla rivi, jossa on **DE – Täytä ALV-palautustietueet**.

   Uusi **Yritys**-kenttä on käytettävissä **Tietolähteiden asetukset** -ruudukossa. Tässä kentässä näkyy aiemmin luotujen tietueiden tapauksessa nykyisen yrityksen tunnus.

5. Lisää **Tietolähteiden asetukset** -ruudukkoon rivi kutakin raportointiin sisällytettävää lisäyritystä varten. Määritä kullekin uudelle riville seuraavat kentät.

    | Kenttä                  | Kuvaus                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nimi                   | Kirjoita arvo, joka auttaa ymmärtämään, mistä tämä tietue tulee. Syötä esimerkiksi **Tytäryhtiön 1 ALV-maksu**. |
    | Sanoman nimiketyyppi      | Valitse **ALV-palautus**. Tämä arvo on ainoa arvo, joka on käytettävissä kaikille tietueille.                                    |
    | Tilityyppi           | Valitse **Kaikki**.                                                                                                               |
    | Päätaulun nimi      | Määritä kaikille tietueille **TaxReportVoucher**.                                                                             |
    | Asiakirjan numerokenttä  | Määritä kaikille tietueille **Voucher**.                                                                                      |
    | Asiakirjan päivämääräkenttä    | Määritä kaikille tietueille **TransDate**.                                                                                    |
    | Asiakirjan tilikenttä | Määritä kaikille tietueille **TaxPeriod**.                                                                                    |
    | Yritys                | Valitse yrityksen tunnus.                                                                                            |
    | Käyttäjän kysely             | Tämä valintaruutu valitaan automaattisesti, kun määrität ehtoja valitsemalla **Muokkaa kyselyä**.                                 |

6. Valitse kullekin uudelle riville **Muokkaa kyselyä** ja määritä liittyvä tilityskausi rivin **Yritys**-kentässä määritetylle yritykselle.

Kun määritys on valmis, **Sähköiset sanomat** -sivun **Kerää tiedot** -toiminto kerää arvonlisäveromaksut kaikilta määritetyiltä yrityksiltä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
