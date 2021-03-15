---
title: Konfiguraatioiden suunnitteleminen asiakirjojen luomiseksi Excel-muodossa
description: Tässä aiheessa käsitellään Excel-mallin täyttävän sähköisen raportointimuodon (ER-muodon) suunnittelua ja lähtevien Excel-muotoisten tiedostojen luontia.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094026"
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
> Jos malli liitetään manuaalisesti, käytettävän [tiedostotyypin](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) on oltava määritetty tätä tarkoitusta varten [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

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

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa](tasks\er-design-reports-openxml-2016-11.md)

[Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja](modify-electronic-reporting-format-reapply-excel-template.md)

[Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäykseen Excel-raportissa](tasks/er-horizontal-1.md)

[Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md)

[Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]