---
title: "Excel-lisäosan käyttö"
description: "Tässä ohjeaiheessa kerrotaan, kuinka avaat yksikkötietoja Microsoft Excelissä ja tarkastelet, päivität ja muokkaat tietoja Microsoft Dynamicsin Excel-lisäosalla."
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: f55e1e89d0e48819962c169a56f0f27dc0d792b4
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# <a name="use-the-excel-add-in"></a>Excel-lisäosan käyttö

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, kuinka avaat yksikkötietoja Microsoft Excelissä ja tarkastelet, päivität ja muokkaat tietoja Microsoft Dynamicsin Excel-lisäosalla. Voit aloittaa yksikkötietojen avaamisen joko Excelistä tai Microsoft Dynamics 365 for Finance and Operations Enterprise editionissa.

Kun avaat yksikkötietoja Microsoft Excelissä, voit tarkastella ja muokata nopeasti tietoja Microsoft Dynamicsin Excel-lisäosalla. Tämä apuohjelma edellyttää, että käytössä on Microsoft Excel 2016. **Huomautus:** jos Microsoft Azure Active Directory (Azure AD) -vuokralaisesi on määritetty käyttämään Active Directoryn liittoutumispalveluita (AD FS), varmista, että toukokuun 2016 päivitys on asennettu, jotta Excel-lisäosa pystyy kirjaamaan sinut sisään.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Yksikkötietojen avaaminen Excelissä Dynamics 365 for Finance and Operationsista käsin
1.  Napsauta Microsoft Dynamics 365 for Finance and Operations -sivulta **Avaa Microsoft Officessa**. Jos sivun juuritietolähde (taulukko) on sama kuin minkä tahansa yksikön juuritietolähde, sivulle muodostetaan oletusasetuksena **Avaa Excelissä**. **Avaa Excelissä** -vaihtoehto löytyy usein käytetyillä sivuilla, kuten **Kaikki toimittajat** ja **Kaikki asiakkaat**.
2.  Valitse **Avaa Excelissä** -vaihtoehto ja avaa luotu työkirja. Tämä työkirja sisältää yksikön sidostiedot, osoitin ympäristöön ja osoitin Excel-lisäosaan.
3.  Valitse Excelin **Ota muokkaus käyttöön** -painike, jotta voit ajaa Excel-lisäosan. Excel-lisäosa toimii Excel-ikkunan oikealla puolella olevassa ruudussa.
4.  Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan**.
5.  Jos näet kirjautumisruudun, valitse **Kirjaudu sisään** samoilla tunnuksilla, joilla kirjaudut Dynamics 365 for Finance and Operationsiin. Excel-lisäosa käyttää aiempaa sisäänkirjautumista Internet Explorerista ja kirjaa sinut sisään automaattisesti, jos se on mahdollista. Varmista tämän vuoksi Excel-lisäosan oikeassa yläkulmassa näkyvä käyttäjänimi.

Excel-lisä lukee valitsemasi yksikön tiedot automaattisesti. Huomaa, että työkirjassa ei ole tietoja ennen kuin Excel-lisäosa on lukenut tiedot.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Avaa yksikön tiedot Excelissä käynnistämisen yhteydessä
1.  Avaa Office-kauppa napsauttamalla **Kauppa**-painiketta Excelin **Lisää**-välilehden **Lisäosat**-ryhmässä.
2.  Etsi Office-kaupasta avainsanalla "Dynamics" ja valitse **Lisää** **Microsoft Dynamicsin Office-lisäosa** (Excel-lisäosa).
3.  Jos käytät Excel-lisäosaa ensimmäistä kertaa, valitse **Luota tähän lisäosaan** voidaksesi käyttää sitä. Excel-lisäosa toimii Excel-ikkunan oikealla puolella olevassa ruudussa.
4.  Avaa **Asetukset**-ruutu napsauttamalla **Lisää palvelimen tiedot** -painiketta.
5.  Kopioi kohteena olevan Dynamics 365 for Finance and Operations -ilmentymän URL-osoite, liitä se **Palvelimen URL-osoite** -kenttään ja poista kaikki teksti isäntänimen jälkeen. URL-osoitteessa tulisi olla vain isäntänimi.
Jos URL-osoite on esimerkiksi https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, poista kaikki paitsi **https://xxx.dynamics.com**.
6.  Vahvista muutokset napsauttamalla **OK** ja sitten **Kyllä**. Excel-lisäosa käynnistyy uudelleen ja lataa metatiedot. **Rakenne**-painike on nyt käytettävissä. Jos Excel-lisäosassa on **Lataa sovelmat** -painike, et ehkä ole kirjautunut oikeana käyttäjänä. Lisätietoja on tämän ohjeaiheen "Vianmääritys"-osan kohdassa "Lataa sovelmat -painike on näkyvissä".
7.  Valitse **Rakenne**. Excel-lisäosa hakee yksikön metatiedot.
8.  Valitse **Lisää taulukko**. Näkyviin tulee luettelo yksiköistä. Yksiköt näytetään muodossa "Nimi – Otsikko".
9.  Valitse luettelosta yksikkö, kuten **Asiakas - Asiakkaat** ja napsauta sitten **Seuraava**.
10. Jos haluat lisätä kentän **Käytettävissä olevat kentät** -luettelosta **Valitut kentät** -luetteloon, napsauta kenttää ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
11. Kun olet lisännyt haluamasi kentät **Valitut kentät** -luetteloon, varmista, että kohdistin on oikeassa kohdassa taulukkoa (esimerkiksi solu A1) ja valitse sitten **Valmis**. Valitse sitten **Valmis** sulkeaksesi suunnitteluohjelman.
12. Valitse **Päivitä** hakeaksesi tietojoukon.

## <a name="view-and-update-entity-data-in-excel"></a>Näytä ja päivitä yksikön tiedot Excelissä
Kun Excel-lisäosa lukee yksikön tiedot työkirjaan, voit päivittää tiedot milloin tahansa valitsemalla Excel-lisäosassa **Päivitä**.

## <a name="edit-entity-data-in-excel"></a>Muokkaa yksikön tietoja Excelissä
Voit muuttaa yksikön tietoja tarpeidesi mukaisesti ja julkaista muutokset takaisin valitsemalla Excel-lisäosassa **Julkaise**. Jos haluat muokata tietuetta, valitse työkirjassa solu ja muuta sitten solun arvoa. Jos haluat lisätä uuden tietueen, seuraa jotakin näistä vaiheista:

-   Napsauta tietolähdetauluun ja valitse sitten **Uusi** Excel-lisäosassa.
-   Valitse tietolähdetaulun viimeinen rivi ja paina sarkainpainiketta, kunnes kohdistin siirtyy pois rivin viimeisestä sarakkeesta ja luo uuden rivin.
-   Napsauta tietolähdetaulun alapuolella olevaa riviä ja aloita tietojen syöttäminen soluun. Kun siirrät kohdistuksen pois solusta, taulu laajentuu uudelle riville.
-   Napsauta otsikkotietueiden kenttäsidoksia varten jotakin kentistä ja sitten **Uusi** Excel-apuohjelmassa.

Huomaa, että uusi tietue luodaan vain, jos kaikki avain- ja pakolliset kentät on sidottu työkirjassa tai jos oletusarvot on täytetty suodatusehdon avulla.
Jos haluat poistaa tietueen, seuraa jotakin näistä vaiheista:

-   Napsauta hiiren kakkospainikkeella poistettavan rivin numeroa työkirjan rivin vieressä ja valitse sitten **Poista**.
-   Napsauta hiiren kakkospainikkeella poistettavaa riviä ja valitse sitten **Poista** &gt; **Taulukon rivit**.
Jos tietolähteitä on lisätty liittyvinä, otsikko julkaistaan ennen rivejä. Jos muiden tietolähteiden välillä on riippuvaisuuksia, joudut ehkä vaihtamaan oletusjulkaisujärjestystä. Julkaisujärjestystä voit muuttaa Excel-apuohjelmassa napsauttamalla **Asetukset**-painiketta (rattaan kuva). Valitse sitten **Data Connector** -pikavälilehdessä **Määritä julkaisujärjestys**.

## <a name="add-or-remove-columns"></a>Lisää tai poista sarakkeita
Voit säätää työkirjaan automaattisesti lisättäviä sarakkeita suunnittelijasovelluksessa.

1.  Käynnistää Excel-lisäosan tietolähteen suunnitteluohjelma napsauttamalla **Asetukset** -painiketta (rattaan kuva) ja valitsemalla sitten **Ota rakenne käyttöön** -valintaruutu.
2.  Valitse Excel-lisäosassa **Rakenne**. Kaikki tietolähteet luetellaan.
3.  Valitse tietolähteen vierestä **Muokkaa**-painike (kynän kuvake).
4.  Muuta **Valitut kentät** -luetteloa tarpeidesi mukaan:
    -   Jos haluat lisätä kentän **Käytettävissä olevat kentät** -luettelosta **Valitut kentät** -luetteloon, napsauta kenttää ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
    -   Voit poistaa kentän **Valitut kentät** -luettelosta napsauttamalla kenttää ja valitsemalla sitten **Poista**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
    -   Jos haluat muuttaa kenttien järjestystä, napsauta kenttää **Valitut kentät** -luettelosta ja sitten **Ylös** tai **Alas**.

5. Ota käyttöön tietolähteeseen tehdyt muutokset valitsemalla **Päivitä**. Valitse sitten **Valmis** sulkeaksesi suunnitteluohjelman. 
6. Jos olet lisännyt kentän (sarakkeen), valitse **Päivitä**, niin ohjelma hakee päivitetyn tietojoukon.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Vianmääritys
Tietyt ongelmat ovat ratkaistavissa muutaman helpon vaiheen kautta.

-   **Lataa sovelmat -painike on näkyvissä.** Jos Excel-lisäosassa on **Lataa sovelmat** -painike kirjautumisen jälkeen, et ehkä ole kirjautunut oikeana käyttäjänä. Ratkaise ongelma varmistamalla, että Excel-lisäosan oikeassa yläkulmassa on oikea käyttäjänimi. Jos näkyvillä on väärä käyttäjänimi, napsauta sitä, kirjaudu ulos ja kirjaudu takaisin sisään.
-   **Näyttöön tulee virhesanoma "Kielletty".** Jos näyttöön tulee virhesanoma "Kielletty", kun Excel-lisäosa lataa metatietoja, Excel-lisäosaan kirjautuneella tilillä ei ole käyttöoikeutta kohteena olevaan palveluun, ilmentymään tai tietokantaan. Ratkaise ongelma varmistamalla, että Excel-lisäosan oikeassa yläkulmassa on oikea käyttäjänimi. Jos näkyvillä on väärä käyttäjänimi, napsauta sitä, kirjaudu ulos ja kirjaudu takaisin sisään.
-   **Excelin päällä näkyy tyhjä verkkosivu.** Jos kirjautumisen aikana avautuu tyhjä verkkosivu, tili vaatii AD FS:n käytön, mutta käytössä oleva Excel-versio ei ole tarpeeksi uusi, että kirjautumisikkunan voisi ladata. Ratkaise ongelma päivittämällä käytössä oleva Excel-versio. Jos olet yritys, jolla on käytössä hidas päivityskanava, voit päivittää Excel-version käyttämällä [Office Deployment Tool -työkalua](https://technet.microsoft.com/library/jj219422.aspx) [vaihtaaksesi hitaan päivityskanavan nykyiseen päivityskanavaan](https://technet.microsoft.com/library/mt455210.aspx).





