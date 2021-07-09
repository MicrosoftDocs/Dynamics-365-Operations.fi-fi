---
title: Viivakoodikuvien luominen viivakoodin tietolähteiden avulla
description: Tässä ohjeaiheessa käsitellään tapaa, jolla viivakoodikuvia voidaan luoda viivakoodin tietolähteiden avulla.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: f72ef77a35c484a40e1384baf69001bba6a333f6
ms.sourcegitcommit: ec272aa133189569abaf4c09b03230611b5a756f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/19/2021
ms.locfileid: "6274533"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Viivakoodikuvien luominen viivakoodin tietolähteiden avulla

[!include[banner](../includes/banner.md)]

Voit suunnitella [sähköisen raportoinnin (ER)](general-electronic-reporting.md) kehikossa [ER-muoto-osia](general-electronic-reporting.md#FormatComponentOutbound), joita suorittamalla voit luoda tarpeen mukaan sähköisiä ja tulostettavia asiakirjoja. Microsoft Office -muotoisen lähtevän asiakirjan luontia varten on määritettävä raportin asettelu käyttämällä raporttimallina joko Microsoft Excel- tai Microsoft Word -tiedostoa. [ER-toimintojen suunnitteluohjelmalla](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) voi liittää Excel- tai Word-tiedoston ER-muodon mallina. Seuraavat liitetyn mallin nimetyt elementit liitetään määritetyn muoto-osan elementteihin:

- Sisällön ohjausobjektit Wordissa
- Nimetyt taulukot, alueet, solut, muodot ja kuvat Excelissä

Näitä nimettyjä elementtejä käytetään niiden tietojen paikkamerkkeinä, jotka luodussa asiakirjassa, kun ER-muoto suoritetaan. ER-muoto-osat sidotaan tietolähteisiin. Nämä tietolähteet määrittävät tiedot, jotka lisätään luoduissa asiakirjoissa suorituksenaikaisesti. Katso lisätietoja kohdasta [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

ER tukee nyt **viivakoodia** tietolähdetyyppinä. Niinpä nyt voi luoda kuvan, joka ilmaisee määritetyn tekstin viivakoodin. ER-muotoa määritettäessä voidaan määrittää viivakoodikuvia luovat **viivakoodi**-tyyppiset tietolähteet. Tämän jälkeen näitä kuvia lisäämällä voidaan luoda liiketoiminta-asiakirjoja, kuten tilauksia, laskuja, pakkausluetteloita ja kuitteja. Ne voidaan lisätä myös erilaisiin etiketteihin, kuten tuote- ja hyllyetiketteihin sekä pakkaus- ja toimitustarroihin.

Viivakoodikuvia voidaan lisätä raporttimalleihin seuraavien paikkamerkkien avulla:

- [Kuva](/office/client-developer/word/content-controls-in-word) Wordin sisällön ohjausobjektina
- [Kuva](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) Excelin objektina

**Viivakoodi**-tyyppisiä tietolähteitä käyttämällä voi luoda seuraavan muotoisia viivakoodeja:

- Yksiulotteiset viivakoodit:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent Mail
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Yksiulotteiset viivakoodit:

    - Aztec
    - Datamatriisi
    - QR-koodi

**Viivakoodi** määritetään tietolähteeksi, kuvan luomisessa käytetyt hahmontamisparametrit voidaan määrittää:

- **Leveys** – Viivakoodin leveys määritetään kuvapisteinä. Arvo **0** (nolla) ilmaisee, että käytössä on oletusleveys. Merkitys voi olla erilainen eri muodoissa.
- **Korkeus** – Viivakoodin korkeus määritetään kuvapisteinä. Arvo **0** (nolla) ilmaisee, että käytössä on oletuskorkeus. Merkitys voi olla erilainen eri muodoissa.
- **Reunus** – Viivakoodin reunus määritetään kuvapisteinä. Reunus on viivakoodin kummallakin puolella oleva alue, jonka on oltava tyhjä (tyhjä tila). Arvo **0** (nolla) ilmaisee, että käytössä on oletusreunus. Merkitys voi olla erilainen eri muodoissa.
- **Tulostesisältö** – Kun arvoksi määritetään **Kyllä**, määritettävä viivakoodikuva sisältää koodatut tiedot tekstinä. Oletusarvo on **Ei**.
- **Koodaus** – Luotuun viivakoodikuvaan koodatun merkkityypin määrittäminen. Oletusarvoisesti käytössä on **UTF-8**-koodaus.

> [!IMPORTANT]
> Kun uusi **Viivakoodi**-tietolähde lisätään, se on sijoitettava toiseen nimikkeeseen (säilöön) sisäkkäisenä elementtinä.
>
> Kun **Viivakoodi**-tietolähde sidotaan muodon soluelementtiin ja soluelementti ilmaisee joko Wordin sisällön ohjausobjektin tai Excelin kuvan, tietolähde ilmaistaan kyseisessä sidonnassa funktiona, jolla on yksi **Merkkijono**-tyyppinen parametri. Tätä parametria on käytettävä määrittämään teksti, joka on muunnettava viivakoodikuvaksi ja luettava, kun luotu viivakoodi luetaan.

Saat lisätietoja tästä toiminnosta suorittamalla tässä ohjeaiheessa olevat esimerkit.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Esimerkki: maksettavan summan koodaavan viivakoodin sisältävän maksun sekin luonti

Tämä esimerkki näyttää, miten käyttäjä, jolla on **järjestelmänvalvojan** tai **sähköisen raportoinnin toiminnallisen konsultin** rooli, voi määrittää sellaisen ER-muodon, joka sisältää Excel-muotoisen viivakoodin sisältävän lähtevän asiakirjan luontiin käytetyn mallin. Yleiskatsaus vaiheista:

1. [Täytä edellytykset](#ExamplePrerequisites).
2. [Aktivoi määrityslähde](#ExampleProvider).
3. [Tuo annettu ER-ratkaisu](#ExampleImportSolution).
4. [Luo maksettava sekki](#ExampleGenerateCheque).
5. [Tarkista luotu maksettava sekki](#ExampleReviewGeneratedCheque).
6. [Muokkaa annetun ER-ratkaisun muotoa](#ExampleModifyFormat).

    1. [Käytä uutta sekkimallia](#ExampleModifyFormatApplyTemplate).
    2. [Lisää uusi Viivakoodi-tietolähde](#ExampleModifyFormatAddDataSource).
    3. [Sido uusi muotoelementti](#ExampleModifyFormatBindFormatElement).
    4. [Tee muokattu versio testiajoja varten](#ExampleModifyFormatMakeVersionAvailable).

        1. [Suorita muokattu muotoversio loppuun](#CompleteToRun).
        2. [Anna luonnosversio käytettäväksi](#MarkToRun).

7. [Luo maksettava sekki](#ExampleGenerateCheque2).
8. [Muunna luotu sekki PDF-tiedostoksi](#ExampleConvertToPDF).

Tässä esimerkissä käytössä on annettu ER-ratkaisu, joka on määritetty luomaan maksettavia sekkejä. Tämä ratkaisu luo maksettavia sekkejä, joissa maksettava summa on kirjoitettu sekä lukuna että tekstinä. Tätä ER-ratkaisua muokataan siten, että sekki sisältää luodun viivakoodin, jossa maksettava summa on koodattu ja joka voidaan lukea viivakoodiskannerilla.

Nämä vaiheet voidaan suorittaa Microsoft Dynamics 365 Financen **USMF**-esimerkkiyrityksessä.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Edellytysten täyttäminen

Tämän esimerkin suorittaminen edellyttää Financessa jonkin seuraavan roolin käyttöoikeutta USMF-yrityksessä:

- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Jos et ole vielä suorittanut tätä esimerkkiä ohjeaiheessa [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md), lataa seuraavat esimerkkinä käytettävän ER-ratkaisun määritykset.

| Sisällön kuvaus         | Tiedostonimi                   |
|-----------------------------|-----------------------------|
| ER-tietomallin konfigurointi | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)      |
| ER-muodon konfigurointi     | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |

Lataa lisäksi seuraava Excel-tiedosto, joka sisältää annetun ER-ratkaisun muokatun mallin.

| Sisällön kuvaus | Tiedostonimi                 |
|---------------------|---------------------------|
| Raporttimalli     | [Check template Excel.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx) |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Aktivoi määrityslähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Tarkista **Lokalisointimääritykset**-sivun **Määrityksen lähteet** -osassa, että näyteyrityksen **Litware, Inc.** [määrityksen lähde](general-electronic-reporting.md#Provider) on luettelossa ja että sen tila on aktiivinen. Jos sitä ei ole luettelossa tai jos sitä ei ole merkitty aktiiviseksi, noudata ohjeaiheen [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) ohjeita.

![Näyteyrityksen määrittäminen aktiiviseksi Lokalisointimääritykset-sivulla](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Annetun ER-ratkaisun tuonti

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Jos **Määritykset**-sivun **Sekkien malli** -määritys ei ole saatavana määrityspuussa, tuo ER-tietomallimääritys seuraavasti:

    1. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
    2. Valitse valintaikkunassa **Selaa**, etsi ja valitse **Model for cheques.xml**-tiedosto ja valitse sitten **OK**.

4. Jos **Sekkien tulostusmuoto** -määritys ei ole saatavana määrityspuussa, tuo ER-muotomääritys seuraavasti:

    1. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
    2. Valitse valintaikkunassa **Selaa**, etsi ja valitse **Cheques printing format.xml**-tiedosto ja valitse sitten **OK**.

5. Laajenna määrityspuussa **Sekkien malli**.
6. Tarkista tuotujen ER-määritysten luettelo määrityspuussa.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Maksettavan sekin luonti

1. Valitse **Maksuliikenteen hallinta** \> **Pankkitilit** \> **Pankkitilit**.
2. Valitse **Pankkitilit**-sivulla **USMF OPER** -tili.
3. Valitse pankkitilin tietosivun toimintoruudun **Määritä**-välilehden **Asettelu**-ryhmässä **Sekki**.
4. Valitse **Sekin asettelu** -sivulla **Muokkaa**.
5. Määritä **Yleiset**-pikavälilehden **Yleinen sähköinen vientimuoto** -asetukseksi **Kyllä**.
6. Valitse **Vie muotokonfiguraatio** -kentässä aiemmin luotu ER-muoto **Sekkien tulostusmuoto**.
7. Valitse toimintoruudussa **Tulosta testi**.
8. Määritä valintaikkunassa **Siirtokelpoinen sekkimuoto** -asetukseksi **Kyllä** ja valitse sitten **OK**.

    ![Sekin asettelu – tulosta testi -valintaikkuna](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Luodun maksettavan sekin tarkistaminen

- Avaa luotu sekki Excelissä.
2. Tarkista luotu sekki.

    ![Luotu maksettava sekki Excelissä](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Annetun ER-ratkaisun muodon muokkaaminen

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Uuden sekkimallin käyttäminen

Voit avata aiemmin tuodun **Cheque template Excel.xlsx** -tiedoston Excelin työpöytäsovelluksella. Huomaa, että malli on erilainen kuin malli, jolla maksettava sekki luotiin annetussa ER-ratkaisussa. Lisäksi se sisältää **AmountBarcode**-elementin viivakoodikuvaa varten.

![AmountBarcode-elementti Excel-mallissa](./media/er-barcode-data-source-cheque2.png)

ER-ratkaisua on nyt muokattava, jonka jälkeen muokattua mallia [käytetään uudelleen](modify-electronic-reporting-format-reapply-excel-template.md).

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Konfiguroinnit**-sivun määrityspuussa **Sekkien malli** ja valitse **Sekkien tulostusmuoto**.
4. Valitse toimintoruudussa **Suunnittelija**.
5. Valitse ER-toimintojen suunnitteluohjelma **Yhdistämismääritys**-välilehti sivun oikealla puolella ja valitse sitten vasemmalla muotopuun ruudussa **Laajenna tai kutista**.
6. Huomaa, että solun kaikki muotoelementit on sidottu sopiviin tietolähteisiin.

    ![Solun muotoelementtien sitominen tietolähteisiin ER-toimintojen suunnitteluohjelmassa](./media/er-barcode-data-source-cells-bound.png)

7. Valitse sivun oikealla puolella **Muoto**-välilehti.
8. Valitse toimintoruudussa ensin kolme pistettä (**...**) ja sitten **Tuo**.
9. Valitse **Tuonti**-ryhmässä **Päivitä Excelissä** ja valitse sitten **Päivitä malli**.
10. Selaa valintaikkunassa tietokoneeseen tallennettuun **Cheque template Excel.xlsx** -tiedostoon ja vahvista sitten valitun mallin käyttö valitsemalla **OK**.
11. Valitse **Yhdistämismääritys**-välilehti sivun oikealla puolella ja valitse sitten vasemmalla muotopuuruudussa **Laajenna tai kutista**.
12. Huomaa, että **AmountBarcode**-soluelementti on lisätty muotoon. Tämä elementti on liitetty **AmountBarcode**-elementtiin, joka on lisätty muokattuun Excel-malliin viivakoodikuvan paikkamerkkinä.

    ![Muotoon ER-toimintojen suunnitteluohjelmassa lisätty AmountBarcode-soluelementti](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Uuden Viivakoodi-tietolähteen lisääminen

Seuraavaksi on lisättävä uusi **Viivakoodi**-tyyppinen tietolähde.

1. Valitse ER-toimintojen suunnitteluohjelmassa sivun oikealla puolella **Yhdistämismääritys**-välilehdessä **tulostus**-tietolähde.
2. Valitse ensin **Lisää** ja sitten **Toiminnot**-ryhmässä **Viivakoodi**-tietolähdetyyppi.

    ![Viivakoodi-tietolähdetyypin valitseminen](./media/er-barcode-data-source-add.png)

3. Kirjoita valintaikkunan **Nimi**-kentässä **viivakoodi**.
4. Valitse **Viivakoodimuoto**-kohdassa **Koodi 128**.
5. Kirjoita **Leveys**-kenttään **500**.
6. Valitse **OK**.

    ![Tietolähteen ominaisuudet -valintaikkuna](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Uuden muotoelementin sitominen

Uusi muotoelementti on sidottava seuraavaksi juuri lisättyyn tietolähteeseen.

1. Valitse ER-toimintojen suunnitteluohjelmassa sivun oikealla **Yhdistämismääritys**-välilehdessä **tulostus\\viivakoodi**-tietolähde.
2. Valitse muotopuuruudun vasemmalla puolella **AmountBarcode**-soluelementti ja valitse sitten **Sido**.
3. Valitse toimintoruudussa **Näytä tiedot**.
4. Huomaa, että koska **Viivakoodi**-tietolähde ilmaistaan sidonnassa toimintona, joka sisältää yhden parametrin, sidotun muotoelementin nimi on otettu automaattisesti kyseisen parametrin argumenttina.

    ![ER-toimintojen suunnitteluohjelman Viivakoodi-tietolähteen tiedot](./media/er-barcode-data-source-bind1.png)

5. Säädä sidontaa valitsemalla **Muokkaa kaavaa**.

    Tämän soluelementin nimeä ei ole nimi, jonka palauttaminen on toivottavaa. Niinpä onkin määritettävä lauseke, joka palauttaa nykyisen sekin maksettavan summan sisältävän tekstin. Koska ylätason **ChequeLines**-alue on sidottu **model.cheques**-tietolähteeseen, nykyisen sekin maksettava summa on saatava **Reaaliluku**-tietotyypin **model.cheques.attributes.amount**-kentässä.

6. Kirjoita **Kaava**-kenttään **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Valitse **Tallenna** ja sulje sitten [ER-muodon suunnitteluohjelma](general-electronic-reporting-formula-designer.md).
8. Huomaa, että sidontaa on säädetty.

    ![Säädetty sidonta ER-toimintojen suunnitteluohjelmassa](./media/er-barcode-data-source-bind2.png)

9. Valitse **Tallenna** ja sulje sitten ER-toimintojen suunnitteluohjelma.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Muokatun version tekeminen testiajoja varten

Oletusarvoisesti vain versioita, joiden tila on **Valmis** tai **Jaettu**, käytetään ER-muotoja suoritettaessa.

Jos muutokset ovat valmiita, nykyisen luonnosversion käsittely voidaan viimeistellä ja muutokset voidaan ottaa käyttöön. Lisätietoja on kohdassa [Muokatun muotoversion suorittaminen loppuun](#CompleteToRun), joka käsitellään seuraavaksi.

Jos nykyisen luonnonversion käsittelyä halutaan jatkaa mutta sitä on käytettävä sekkien luontiin, on nimenomaisesti määritettävä, että suorittamisessa halutaan käyttää muodon luonnosversiota. Lisätietoja on kohdassa [Luonnosversion antaminen käytettäväksi](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Muokatun muotoversion suorittaminen loppuun

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Laajenna **Konfiguroinnit**-sivun määrityspuussa **Sekkien malli** ja valitse **Sekkien tulostusmuoto**.
4. Valitse **Versiot**-pikavälilehdessä tietue, jonka tila on **Luonnos**.
5. Valitse **Muuta tilaa** ja valitse sitten **Valmis**.
6. Valitse valintaikkunassa **OK**.

Nykyisen versio **Luonnos**-tila muuttuu **Valmis**-tilaksi ja uusi versio, jonka tila on **Luonnos**-luodaan. Lisämuutoksia voi käyttää tässä uudessa luonnosversiossa.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Luonnosversion antaminen käytettäväksi

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Lokalisointimääritykset**-sivun **Konfiguroinnit**-osassa **Raportointimääritykset**-ruutu.
3. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
4. Määritä valintaikkunassa **Suorita asetus** -asetukseksi **Kyllä** ja valitse sitten **OK**.
5. Laajenna määrityspuussa **Sekkien malli** ja valitse **Sekkien tulostusmuoto**.
6. Määritä **Suorita luonnos** -vaihtoehdoksi **Kyllä**.
7. Valitse **Tallenna**.

Valitun muodon luonnosversio merkitään käytettäväksi, kun valittu muoto suoritetaan.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Maksettavan sekin luonti

1. Valitse **Maksuliikenteen hallinta** \> **Pankkitilit** \> **Pankkitilit**.
2. Valitse **Pankkitilit**-sivulla **USMF OPER** -tili.
3. Valitse pankkitilin tietosivun toimintoruudun **Määritä**-välilehden **Asettelu**-ryhmässä **Sekki**.
4. Valitse **Sekin asettelu** -sivulla toimintoruudussa **Tulosta testi**.
5. Määritä valintaikkunassa **Siirtokelpoinen sekkimuoto** -asetukseksi **Kyllä**.
6. Valitse **OK**.
7. Tarkista luotu sekki. Huomaa, että viivakoodi on luotu koodaamaan sekin maksettava summa.

    ![Excelissä luotu viivakoodin sisältävä maksettava sekki](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Poikkeus annetaan, jos **Viivakoodi**-tietolähteen argumentti ei vastaa viivakoodimuodolle ominaisia vaatimuksia. Jos esimerkiksi **Viivakoodi**-tietolähde käynnistetään luomaan [EAN-8](https://wikipedia.org/wiki/EAN-8)-viivakoodi annetulle tekstille, poikkeus annetaan, jos tekstin pituus ylittää seitsemän merkkiä.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Luodun sekin muuntaminen PDF-tiedostoksi

Kuten ohjeaiheessa [Tulostettavien FTI-lomakkeiden luominen](er-generate-printable-fti-forms.md#finland) on kuvattu, erikoisfonttia voi käyttää viivakoodin tuottamiseen luodussa asiakirjassa. Tässä tapauksessa luodun asiakirjan lisämuunnokset voivat määräytyä sen mukaan, onko kyseinen fontti käytettävissä muunnosympäristössä. Jos asiakirja yritetään esimerkiksi muuntaa PDF-muotoon tai jos sitä yritetään esikatsella ympäristössä, josta fontti puuttuu, viivakoodeja ei hahmonneta oikein.

Jos viivakoodit kuitenkin tuotetaan käyttämällä **Viivakoodi**-tietolähdettä, kyseisten viivakoodien hahmonnus ei määräydy minkään fontin mukaan. Tämän vuoksi viivakoodeja sisältävien asiakirjojen muuntaminen PDF-muotoon on helppoa. Seuraavassa kuvassa on sellaisen luodun maksettavan sekin esikatselu, joka on [muunnettu](electronic-reporting-destinations.md#OutputConversionToPDF) PDF-muotoon määritetyn ER-[kohteen](electronic-reporting-destinations.md) asetuksen mukaan.

![Maksettavan sekin PDF-muodon esikatselu](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Rajoitukset

> [!NOTE]
> Joillakin luoduilla viivakoodityypeillä on kiinteä kuvasuhde. Tästä on hyötyä silloin, jos **Ota EPPlus-kirjasto käyttöön sähköisen raportoinnin kehyksessä** -toiminto on otettu käyttöön Excel-asiakirjojen käsittelemiseen sähköisessä raportoinnissa. Siinä tapauksessa paikkamerkkiin annetussa kuvassa on lukittu kuvasuhde. Niinpä kun mallin paikkamerkin mitat vastaavat annetun kuvan suhdetta, luodussa asiakirjassa olevan varsinaisen kuvan kokoa voidaan muuttaa, jotta vaadittavaa kuvasuhdetta ylläpidetään. Kuvan koon muuttamisen voi estää käyttämällä paikkamerkkiä, jossa on odotettu kuvasuhde.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kohteet](electronic-reporting-destinations.md)
- [Sähköisen raportoinnin kaavakieli](er-formula-language.md)
- [NUMBERFORMAT-funktio](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
