---
title: Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa
description: Tässä aiheessa käsitellään Excel-mallin täyttävän sähköisen raportointimuodon (ER-muodon) suunnittelua ja lähtevien Excel-muotoisten tiedostojen luontia.
author: NickSelin
manager: AnnBe
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82afcdeb45bad79a008c3135ef332cf01c0b580
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574170"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Excel-muotoisia tiedostoja luovan määrityksen suunnitteleminen

[!include[banner](../includes/banner.md)]

Voit suunnitella [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muotomäärityksen, jonka ER[-muoto-osan](general-electronic-reporting.md#FormatComponentOutbound) voi määrittää luomaan lähtevän tiedoston Microsoft Excel -muotoisena työkirjana. Tätä tarkoitusta varten on käytettävä tiettyjä ER-muoto-osia.

Lisätietoja tästä toiminnosta on ohjeaiheen [Konfiguraation suunnitteleminen raporttien luomiseksi OPENXML-muodossa](tasks/er-design-reports-openxml-2016-11.md) ohjeissa.

## <a name="add-a-new-er-format"></a>Uuden ER-muodon lisääminen

Kun Excel-työkirjamuotoisen lähtevän tiedoston luontia varten lisätään uusi ER-muotomääritys, muodon **Muodon tyyppi** -määritteeksi on joko valittava **Excel**-arvo tai **Muodon tyyppi** -määrite on jätettävä tyhjäksi.

- Jos valitse **Excel**, muoto voidaan määrittää luomaan lähtevä tiedosto vain Excel-muodossa.
- Jos määrite jätetään tyhjäksi, voit määrittää lähtevän tiedoston luovaksi muodoksi minkä tahansa ER-kehyksen tukeman muodon.

Määrityksen Er-muoto-osa määritetään valitsemalla toimintoruudussa **Suunnitteluohjelma** ja avaamalla ER-muoto-osa muokattavaksi ER-toiminnon suunnitteluohjelmassa.

![Konfiguroinnit-sivu](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-tiedosto-osa

### <a name="manual-entry"></a>Manuaalinen kirjaus

**Excel\\Tiedosto**-osa on lisättävä määritettyyn ER-muotoon luomaan lähtevä tiedosto Excel-muodossa.

![Excel\Tiedosto-osa](./media/er-excel-format-add-file-component.png)

Lähtevän tiedoston asettelu määritetään liittämällä Excel-työkirja, jossa on .xlsx-tunniste, **Excel\\Tiedosto**-osaan lähtevien tiedostojen mallina.

> [!NOTE]
> Jos malli liitetään manuaalisesti, käytettävän [tiedostotyypin](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) on oltava määritetty tätä tarkoitusta varten [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Liitteen lisääminen Excel\Tiedosto-osaan](./media/er-excel-format-add-file-component2.png)

Voit määrittää tavan, jolla liitetty malli täytetään määritettyä ER-muotoa suoritettaessa, lisäämällä sisäkkäiset **Taulukko**-, **Alue**- ja **Solu**-osat **Excel\\Tiedosto**-osaan. Kukin sisäkkäinen osa on liitettävä Excelin nimettyyn kohteeseen.

### <a name="template-import"></a>Mallin tuonti

Uusi malli voidaan tuoda tyhjään ER-muotoon valitsemalla **Tuo Excelistä** toimintoruudun **Tuonti**-välilehdessä. Tässä esimerkissä **Excel\\Tiedosto**-osa luodaan automaattisesti ja tuotu malli liitetään siihen. Myös kaikki pakolliset ER-osat luodaan automaattisesti löydetyn Excelin nimettyjen kohteiden luettelon perusteella.

![Tuo Excelistä -toiminnon valinta](./media/er-excel-format-import-template.png)

> [!NOTE]
> Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.

## <a name="sheet-component"></a>Taulukko-osa

**Taulukko**-osa ilmaisee sen liitetyn Excel-työtyökirjan laskentataulukon, joka on täytettävä. Excel-mallissa olevan laskentataulukon nimi määritetään tämän osan **Taulukko**-ominaisuudessa.

> [!NOTE]
> Tämä osa on valinnainen vain yhden laskentataulukon sisältävissä Excel-työkirjoissa.

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Taulukko**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva laskentataulukko asetetaan luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, luotu tiedosto ei sisällä laskentataulukkoa.

![Esimerkki Taulukko-osasta](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Alue-osa

**Alue**-osa ilmaisee Excel-alueen, joka on oltava tämän ER-osan hallinnassa. Alueen nimi määritetään tämän osan **Excel-alue**-ominaisuudessa.

**Replikointisuunta**-ominaisuus määrittää, toistetaanko alue luodussa tiedostossa ja millä tavoin se toistetaan:

- Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Ei replikointia**, soveltuvaa Excel-aluetta ei toisteta luodussa tiedostossa.
- Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Pystysuuntainen**, soveltuvaa Excel-alue toistetaan luodussa tiedostossa. Jokainen replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen alapuolelle. Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.
- Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Vaakasuuntainen**, soveltuvaa Excel-alue toistetaan luodussa tiedostossa. Jokainen replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen oikealle puolelle. Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.

Lisätietoja vaakasuuntaisesta replikoinnista on kohdan [Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin](tasks/er-horizontal-1.md) ohjeissa.

**Alue**-osassa voi olla muita sisäkkäisiä ER-osia, joiden avulla annetaan arvoja soveltuvilla Excelin nimetyillä alueilla.

- Jos arvoja annetaan jollakin **Teksti**-ryhmän osalla, arvo annetaan Excel-alueella tekstiarvona.

    > [!NOTE]
    > Tämän mallin avulla voi muotoilla annettuja arvoja sovelluksen määritettyjen alueasetusten perusteella.

- Jos **Excel**-ryhmän **Solu**-osaa käytetään arvojen antamiseen, arvo annetaan Excel-alueelle sen tietotyypin arvona, joka on määritetty kyseisen **Solu**-osan sidonnalla (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**).

    > [!NOTE]
    > Tämän mallin avulla Excel-sovelluksessa voidaan ottaa käyttöön annettujen arvojen muotoilu sen paikallisen tietokoneen alueasetusten perusteella, joka avaa lähtevän tiedoston.

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Alue**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva alue täytetään luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue ei vastaa kokonaisia rivejä tai sarakkeita, sopivaa aluetta ei täytetä luotuun tiedostoon.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue vastaa kokonaisia rivejä tai sarakkeita, luoto tiedosto sisältää kyseiset rivit ja sarakkeet piilotettuina riveinä ja sarakkeina.

## <a name="cell-component"></a>Solu-osa

**Solu**-osaa käytetään täyttämään Excelin nimetyt solut, muodot ja kuvat. Sellainen Excelin nimetty objekti, jonka **Solu**-ER-osan on täytettävä, ilmaistaan määrittämällä kyseisen objektin nimi **Solu**-osan **Excel-alue**-ominaisuudessa.

ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Solu**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko objekti täytettävä luodussa tiedostossa.

- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva objekti täytetään luodussa tiedostossa. Tämän **Solu**-osan sidonta määrittää arvo, joka sijoitetaan sopivaan objektiin.
- Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, sopivaa objektia ei täytetä luodussa tiedostossa.

Jos **Solu**-osa on määritetty antamaan solun arvo, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**). Tässä tapauksessa arvo annetaan solussa saman tietotyypin arvona.

Jos **Solu**-osa on määritetty antamaan arvo Excel-muotona, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**). Tässä tapauksessa arvo annetaan Excel-muodossa kyseisen muodon tekstinä. Muissa kuin **Merkkijono**-tietotyypin arvoissa muunto tekstiksi tehdään automaattisesti.

> [!NOTE]
> **Solu**-osan voi määrittää täyttämään muodon vain tapauksissa, joissa muodon tekstiominaisuutta tuetaan.

Jos **Solu**-osa on määritetty antamaan arvo Excel-kuvana, se voidaan sitoa tietolähteeseen, joka palauttaa kuvan binaarimuodossa ilmaisevan **Säilö**-tyypin arvon. Tässä tapauksessa arvo annetaan Excel-kuvassa kuvana.

> [!NOTE]
> Jokainen Excel-kuva ja -muoto katsotaan ankkuroiduksi vasemmasta yläkulmasta tiettyyn Excel-soluun tai -alueeseen. Jos Excel-kuva tai -muoto halutaan replikoida, se solu tai alue, johon se on ankkuroitu, on määritettävä replikoiduksi soluksi tai alueeksi.

Lisätietoja kuvien ja muotojen upottamisesta on kohdassa [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Sivunvaihto-osa

**Sivunvaihto**-osa pakottaa Excelin aloittamaan uuden sivun. Tämä osa ei ole pakollinen, jos haluat käyttää Excelin oletussivusta, mutta sitä kannattaa käyttää, jos haluat Excelin jäsentävän sivutuksen ER-muodon mukaisesti.

## <a name="footer-component"></a>Alatunnistekomponentti

**Alatunniste**-komponentin avulla täytetään Excel-työkirjassa luodun laskentataulukon alaosaan alatunniste.

> [!NOTE]
> Voit lisätä tämän komponentin jokaiselle **Laskentataulukko**-komponentille määrittääksesi eri alatunnisteet luodun Excel-työkirjan eri laskentataulukoille.

Kun määrität yksittäisen **Alatunniste**-komponentin, voit **Otsikon/alatunnisteen ulkoasu** -ominaisuuden avulla määrittää sivut, joissa komponenttia käytetään. Käytettävissä ovat seuraavat arvot:

- **Kaikki** – Suorita määritetty **Alatunniste**-komponentti kaikille Excel-päälaskentataulukon sivuille.
- **Ensimmäinen** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon ensimmäiselle sivulle.
- **Parillinen** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon parillisille sivuille.
- **Pariton** – Suorita määritetty **Alatunniste**-komponentti vain Excel-päälaskentataulukon parittomille sivuille.

Voit lisätä yksittäiselle **Laskentataulukko**-komponentille useita **alatunniste**-komponentteja, joilla kullakin on eri arvo **Otsikon/alatunnisteen ulkoasu** -ominaisuudelle. Näin voit luoda eri alatunnisteita Excel-laskentataulukon erityyppisille sivuille.

> [!NOTE]
> Varmista, että jokaiselle yksittäiselle **Laskentataulukko**-komponentille lisätylle **Alatunniste**-komponentilla on eri arvo **Otsikon/alatunnisteen ulkoasu** -ominaisuudelle. Muussa tapauksessa tapahtuu [oikeellisuustarkistusvirhe](er-components-inspections.md#i16). Näyttöön tulee virhesanoma, joka ilmoittaa epäyhtenäisyydestä.

Lisää lisätyn **alatunniste**-komponentin kohdassa sisäkkäiset komponentit **Text\\String**, **Text\\DateTime** tai muu tyyppi. Määritä näiden komponenttien sidonnat ja määritä, miten sivun alatunniste täytetään.

Erityisten [muotoilukoodien](https://docs.microsoft.com/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) avulla voit muotoilla luodun alatunnisteen sisällön oikein. Lisätietoja tämän menetelmän käytöstä on jäljempänä tässä ohjeaiheessa [esimerkin 1](#example-1) vaiheiden mukaisesti.

> [!NOTE]
> Kun määrität ER-muotoja, muista ottaa huomioon Excelin [rajoitus](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) ja yksittäisen ylä- tai alatunnisteen enimmäismerkkimäärä.

## <a name="header-component"></a>Ylätunnistekomponentti

**Ylätunniste**-komponentin avulla täytetään Excel-työkirjassa luodun laskentataulukon yläosaan ylätunniste. Sitä käytetään kuten **Alatunniste**-komponenttia.

## <a name="edit-an-added-er-format"></a>Lisätyn ER-muodon muokkaaminen

### <a name="update-a-template"></a>Mallin päivittäminen

Päivitetty malli voidaan tuoda muokattavaan ER-muotoon valitsemalla **Päivitä Excelistä** toimintoruudun **Tuonti**-välilehdessä. Valitun **Excel\\Tiedosto**-osan malli korvataan uudella mallin tämän prosessin aikana. Muokattavan ER-muodon sisältö synkronoidaan päivitetyn ER-mallin sisällön kanssa.

- Jokaiselle Excel-nimelle luodaan automaattisesti uusi ER-muoto, jos muokattavassa muodossa olevaa ER-muoto-osaa ei löydy.
- Jokainen ER-muoto-osa on poistettava muokattavasta ER-muodosta, jos sille ei löydy sopivaa Excel-nimeä.

> [!NOTE]
> Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.
>
> Jos muokattavassa ER-muoto sisälsi alun perin **Taulukko**-elementtejä, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä** päivitettyä mallia tuotaessa. Muussa tapauksessa kaikki alkuperäisen **Taulukko**-elementin sisäkkäiset elementit luodaan alusta. Tämän vuoksi kaikki uudelleenluotujen muotoelementtien sidonnat menetetään päivitetyssä ER-muodossa.

![Luo Excel-taulukkomuotoinen elementti -vaihtoehto Päivitä Excelistä -valintaikkunassa](./media/er-excel-format-update-template.png)

Lisätietoja tästä toiminnosta on kohdan [Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja uudelleen](modify-electronic-reporting-format-reapply-excel-template.md) ohjeissa.

## <a name="validate-an-er-format"></a>ER-muodon vahvistaminen

Muokattavaa ER-muotoa vahvistettaessa tehdään yhdenmukaisuustarkistus, jolla varmistetaan, että Excel-nimi esiintyy käytettävässä Excel-mallissa. Saat ilmoituksen mahdollisista ristiriidoista. Joidenkin ristiriitojen osalta tarjotaan mahdollisuutta korjata ongelmat automaattisesti.

![Vahvistusvirhesanoma](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Excel-kaavojen laskemisen hallinta

Kun Microsoft Excel -työkirjamuodossa oleva lähtevä asiakirja luodaan, jotkin tämän asiakirjan solut voivat sisältää Excel-kaavoja. Kun **Ota käyttöön EPPlus-kirjaston sähköinen raportointijärjestelmä** -toiminto on käytössä, voit määrittää, milloin kaavat lasketaan, muuttamalla **Laskentavalinnat**-[parametrin](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) arvoa käytetyssä Excel-mallissa:

- Valitse **Automaattinen**, jos haluat laskea kaikki riippuvaiset kaavat uudelleen aina, kun luotu tiedosto liitetään uusilla alueilla, soluissa jne.
    >[!NOTE]
    > Tämä saattaa aiheuttaa suorituskykyongelman niille Excel-malleille, jotka sisältävät useita toisiinsa liittyviä kaavoja.
- Valitse **Manuaalinen**, jos haluat välttää kaavojen uudelleenlaskennan, kun asiakirja luodaan.
    >[!NOTE]
    > Kaavan uudelleenlaskenta pakotetaan manuaalisesti, kun luotu asiakirja avataan esikatselua varten Excelissä.
    > Älä käytä tätä vaihtoehtoa, jos määrität ER-kohteen, joka olettaa, että luotu tiedosto on käytössä ilman sen esikatselua Excelissä (PDF-muunnos, sähköpostin lähetys jne.) koska luotu tiedosto ei ehkä sisällä kaavoja sisältävien solujen arvoja.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Esimerkki 1: Alatunnisteen sisällön muotoileminen

1. Käyttämällä ER-konfiguraatioita voit [luoda](er-generate-printable-fti-forms.md) tulostettavan vapaatekstilaskun (FTI) asiakirjan.
2. Tarkista luodun tiedoston alatunniste. Huomaa, että sivu sisältää tietoja nykyisestä sivunumerosta ja asiakirjan sivujen kokonaismäärästä.

    ![Luodun tiedoston alatunnisteen tarkasteleminen Excel-muodossa](./media/er-fillable-excel-footer-1.gif)

3. [Avaa](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ER-muodon suunnittelijassa tarkistettavaksi ER-esimerkkimuoto.

    **Lasku**-laskentataulukon alatunniste luodaan kahden **Alatunniste**-komponentissa olevan **Merkkijono**-komponentin asetusten perusteella:

    - Ensimmäinen **merkkijono**-osa täyttää seuraavat erityismuotoilukoodit, jotka pakottavat Excelin käyttämään tiettyjä muotoiluja:

        - **&C** – Tasaa alatunnisteteksti keskelle.
        - **&"Segoe UI,Regular"&8** – Esittää alatunnisteen tekstin "Segoe UI Regular" -fontilla, jonka koko on 8 pistettä.

    - Toinen **merkkijono**-komponentti lisää tekstin, joka sisältää nykyisen sivunumeron ja nykyisen asiakirjan sivujen kokonaismäärän.

    ![Alatunnisteen ER-muotokomponentin tarkistus Muodon suunnittelija -sivulla](./media/er-fillable-excel-footer-2.png)

4. Muokkaa nykyisen sivun alatunnistetta mukauttamalla ER-esimerkkimuotoa:

    1. [Luo](er-quick-start2-customize-report.md#DeriveProvidedFormat) johdettu **Vapaatekstilasku (Excel) mukautettu** ER-muoto, joka perustuu ER-esimerkkimuotoon.
    2. Lisää **Lasku**-laskentataulukon **Alatunniste**-komponentin ensimmäiset uudet **merkkijono**-komponentit:

        1. Lisää **merkkijono**-komponentti, joka tasaa yrityksen nimen vasemmalle ja esittää sen 8 pisteen "Segoe UI Regular" -fontilla (**"&L&"Segoe UI,Regular"&8"**).
        2. Lisää **merkkijono**-komponentti, joka täyttää yrityksen nimen (**model.InvoiceBase.CompanyInfo.Name**).

    3. Lisää **Lasku**-laskentataulukon **Alatunniste**-komponentin toiset uudet **merkkijono**-komponentit:

        1. Lisää **merkkijono**-komponentti, joka tasaa käsittelypäivämäärän oikealle ja esittää sen 8 pisteen "Segoe UI Regular" -fontilla (**"&R&"Segoe UI,Regular"&8"**).
        2. Lisää **merkkijono**-komponentti, joka täyttää käsittelypäivämäärän mukautetussa muodossa (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Alatunnisteen ER-muotokomponentin tarkistus Muodon suunnittelija -sivulla](./media/er-fillable-excel-footer-3.png)

    4. [Viimeistele](er-quick-start2-customize-report.md#CompleteDerivedFormat) johdetun **Vapaatekstilasku (Excel) mukautettu** -ER-muodon luonnosversio.

5. [Määritä](er-generate-printable-fti-forms.md#configure-print-management) tulostuksenhallinta käyttämään johdettua **Vapaatekstilasku (Excel) mukautettu** -ER-muotoa ER-esimerkkimuodon sijaan.
6. Luo tulostettava FTI-tiedosto ja tarkista luodun tiedoston alatunniste.

    ![Luodun tiedoston alatunnisteen tarkasteleminen Excel-muodossa](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](tasks\er-design-reports-openxml-2016-11.md)

[Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja](modify-electronic-reporting-format-reapply-excel-template.md)

[Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäykseen Excel-raportissa](tasks/er-horizontal-1.md)

[Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

[Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
