---
title: "Excel-apuohjelman käyttäminen"
description: "Tässä ohjeaiheessa kerrotaan, kuinka avata kohteen tiedot Microsoft Excelissä ja tarkastella, päivittää ja muokata tietoja käyttämällä Microsoft Dynamics Office-apuohjelman Exceliin. Avaa kohteen tiedot, voit käynnistää Excelin tai Microsoft Dynamics-365 operaatioille."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Excel-apuohjelman käyttäminen

Tässä ohjeaiheessa kerrotaan, kuinka avata kohteen tiedot Microsoft Excelissä ja tarkastella, päivittää ja muokata tietoja käyttämällä Microsoft Dynamics Office-apuohjelman Exceliin. Avaa kohteen tiedot, voit käynnistää Excelin tai Microsoft Dynamics-365 operaatioille.

Avaamalla kohteen tiedot Microsoft Excelissä nopeasti ja helposti tarkastella ja muokata tietoja käyttämällä Microsoft Dynamics Office-apuohjelman Exceliin. Tämä apuohjelma edellyttää Microsoft Excel-2016. **Huomautus:** Jos Microsoftin Azure Active Directory (Azure AD)-vuokralaisen on määritetty käyttämään Active Directory Federation Services (AD FS), varmista, että toukokuun 2016-päivitys on asennettu, niin, että Excel-apuohjelma voi oikein kirjautuminen.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Avaa entiteetin tietoja Excelissä, kun käynnistetään toimintoja varten 365 Dynamics
1.  Microsoft Dynamics-365 toimintoja varten-sivulle, valitse **Avaa Microsoft Office-**. Jos sivun juuritietolähde (taulukko) on sama kuin juuritietolähde entiteettejä, oletus **avaa Excelin** muodostetaan sivun asetukset. **Avaa Excelin** vaihtoehtoja löytyy usein sivuilla, kuten **kaikkien toimittajien** ja **kaikille asiakkaille**.
2.  Valitse **avata Excelissä** asetus ja Avaa työkirja, joka on luotu. Tämä työkirja on sitovan tiedon yksikkö, osoitin ympäristön ja osoittimen Excel-apuohjelma.
3.  Valitse Excelin **muokkausta** Excel-apuohjelman suorittamisen mahdollistamiseksi. Excel-apuohjelma toimii ruudussa Excel-ikkunan oikealla puolella.
4.  Jos käytät Excel-apuohjelma ensimmäistä kertaa, valitse **luota tämän**.
5.  Jos sinua pyydetään kirjautumisen, valitse **kirjautua sisään**, ja sitten Kirjaudu sisään käyttäen, jota käytit Dynamics 365 työvaiheiden kirjautua samoilla tunnistetiedoilla. Excelin apuohjelman tulee käyttää edellisen sisään kontekstin ja poistaa Internet Explorer ja Kirjaudu automaattisesti, jos se on mahdollista. Varmista tämän vuoksi Excelin apuohjelman oikeassa yläkulmassa käyttäjänimi.

Excel-apuohjelma lukee automaattisesti valitsemasi entiteetin tietoja. Huomaa, että siellä ei ole tietoja työkirjan Excel-apuohjelma lukee sitä ennen.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Avaa entiteetin tietoja Excelissä Excelin käynnistämisen yhteydessä
1.  Excelissä- **Lisää** -lehden **-apuohjelmat** ryhmän, valitse **myymälän** Office-säilön avaaminen.
2.  Etsi Office-myymälän avainsanan "Dynamics" ja valitse **Lisää** vieressä **Dynamics Microsoft Office-apuohjelma** (Excelin apuohjelma).
3.  Jos käytät Excel-apuohjelma ensimmäistä kertaa, valitse **luota tämän** Excel-apuohjelman suorittamisen mahdollistamiseksi. Excel-apuohjelma toimii ruudussa Excel-ikkunan oikealla puolella.
4.  Valitse **Lisää palvelimen tiedot** avaamiseen **asetukset** ruutu.
5.  Kopioi URL-osoite selaimen toimintojen esiintymän kohde Dynamics 365, liittää sen sovellukseen **palvelimen URL-osoite** kenttään ja poista kaikki isännän nimen jälkeen (esimerkiksi poistaa **/? cmp = usmf & mi = CustTableListPage**). Tuloksena URL-Osoitteen on oltava isännän nimi (esimerkiksi **https://xxx.dynamics.com**).
6.  Valitse **OK**, ja sitten **Kyllä** vahvistamaan muutoksen. Excel lisää käynnistyy ja lataa metatiedot. **Rakenne** painike on nyt käytettävissä. Jos Excel-apuohjelma on **ladata sovelmat** -painiketta, et ehkä ole kirjautunut käyttäjänä, oikea. Lisätietoja on tämän ohjeaiheen kohdassa "Vianmääritys" "kuormituksen sovelmat painike näkyy".
7.  Valitse **rakenne**. Excel-apuohjelma hakee yksikön metatietoja.
8.  Valitse **Lisää taulukko**. Tulee kohteiden luettelo. Entiteetit näkyvät muodossa "Nimi – otsikko".
9.  Valitse kohde luettelosta, kuten **asiakas - asiakkaille**, ja sitten **seuraavan**.
10. Lisää kenttä **käytettävissä olevat kentät** luettelossa **valitut kentät** luettelosta, napsauta kenttää ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
11. Kun olet lisännyt haluamasi kentät **valitut kentät** luettelossa, varmista, että kohdistin on oikea paikka taulukon (esimerkiksi solu A1) ja valitse sitten **tehty**. Valitse **tehty** Sulje suunnitteluohjelma.
12. Valitse **päivittää** voit saada näkyviin tietoja.

## <a name="view-and-update-entity-data-in-excel"></a>Näytä ja Päivitä kohteen tietoja Excelissä
Kun Excel-apuohjelma lukee entiteetin tietoja työkirjaan, voit päivittää tiedot milloin tahansa valitsemalla **päivittää** Excel-apuohjelman.

## <a name="edit-entity-data-in-excel"></a>Muokkaa entiteetin tietoja Excelissä
Voit muuttaa entiteetin tietoja edellyttää ja julkaista sen sitten uudelleen valitsemalla **Julkaise** Excel-apuohjelman. Jos haluat muokata tietuetta, valitse laskentataulukon soluun ja sitten muuttaa solun arvon. Jos haluat lisätä uuden tietueen, tekemällä jommankumman seuraavista seuraavasti:

-   Napsauta taulukon ja valitsemalla sitten **uusi** Excel-apuohjelman.
-   Valitse laskentataulukon viimeisen rivin, ja paina SARKAINTA, kunnes kohdistin siirtyy rivin viimeisen sarakkeen ulkopuolella ja luodaan uusi rivi.
-   Napsauta taulukon alapuolella olevan rivin ja alat kirjoittaa tietoja soluun. Kun siirrät kohdistuksen soluun pois, laskentataulukon lisääntyvät uuden rivin.

Jos haluat poistaa tietueen, tekemällä jommankumman seuraavista seuraavasti:

-   Napsauta hiiren kakkospainikkeella rivin numeron taulukon rivin vieressä Jos haluat poistaa, ja valitse sitten **poistaa**.
-   Poista taulukon riviä hiiren kakkospainikkeella ja valitse sitten **poistaa**&gt;**taulukon rivien**.

## <a name="add-or-remove-columns"></a>Lisää tai poista sarakkeita
Voit säätää sarakkeet, jotka lisätään automaattisesti taulukon suunnittelija.

1.  Käynnistää tietojen lähde suunnittelija Excel-apuohjelma napsauttamalla **asetukset** (vaihde symboli)-painiketta ja valitsemalla sitten **käyttöön rakenne** valintaruutu.
2.  Valitse **rakenne** Excel-apuohjelman. Kaikki tietolähteet luetellaan.
3.  Tietolähde-kohdan vierestä **Muokkaa** painike (kynäsymboli).
4.  Muuta luettelon **valitut kentät** niin, että luettelo:
    -   Lisää kenttä **käytettävissä olevat kentät** luettelossa **valitut kentät** luettelosta, napsauta kenttää ja valitse sitten **Lisää**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
    -   Jos haluat poistaa kentän **valitut kentät** luettelosta, napsauta kenttää ja valitse sitten **poistaa**. Vaihtoehtoisesti voit kaksoisnapsauttaa kenttää.
    -   Voit muuttaa kenttien järjestystä, napsauta kenttää **valitut kentät** luettelosta ja napsauta sitten **ylös** tai **alas**.

5.  Muutokset tietolähteeseen valitsemalla **päivitys**. Valitse **tehty** Sulje suunnitteluohjelma. Jos olet lisännyt kentän (sarakkeen), valitse **päivittää** vetämään tiedot päivitetty joukko.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
On joitakin ongelmia, jotka voidaan ratkaista joitakin helpon vaiheen kautta.

-   **Kuormituksen sovelmat-painike on näkyvissä.** Jos Excel-apuohjelma on **ladata sovelmat** painiketta jälkeen Kirjaudu sisään, et ehkä ole kirjautunut oikea käyttäjänä. Voit ratkaista tämän ongelman, tarkista oikea käyttäjänimi näkyy Excelin apuohjelman oikeassa yläkulmassa. Näyttöön tulee virheellisen käyttäjänimen, jos napsauttamalla sitä, kirjaudu ulos ja kirjaudu sitten takaisin sisään.
-   **Näyttöön tulee virhesanoma "Kielletty".** Jos näyttöön tulee virhesanoma "Kielletty", kun taas Excel-apuohjelma ladataan metatietoja, tili, joka on kirjautunut Excel-apuohjelma ei ole oikeutta käyttää kohdennettua palvelua, esiintymän tai tietokannan. Voit ratkaista tämän ongelman, tarkista oikea käyttäjänimi näkyy Excelin apuohjelman oikeassa yläkulmassa. Näyttöön tulee virheellisen käyttäjänimen, jos napsauttamalla sitä, kirjaudu ulos ja kirjaudu sitten takaisin sisään.
-   **Tyhjä WWW-sivulla näkyy Excelin kautta.** Sisään aikana avautuu tyhjä sivu, jos tili edellyttää AD FS, mutta apuohjelma, jossa on Excel-version ei ole viimeisimmät Lataa Kirjaudu sisään valintaikkunassa. Tämän ongelman ratkaisemiseksi, joita käytät Excel-version päivittäminen Voit päivittää Excel-version olet yritys, joka on lykätty kanavalla [Office deployment Tool-työkalua](https://technet.microsoft.com/library/jj219422.aspx), [siirtyminen laskennallinen kanavan nykyisen kanavan](https://technet.microsoft.com/library/mt455210.aspx).



