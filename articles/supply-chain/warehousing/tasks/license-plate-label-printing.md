--- 
title: "Ota käyttöön rekisterikilven etiketin tulostus"
description: "Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Ota käyttöön rekisterikilven etiketin tulostus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näin sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa. Voit suorittaa tämän menettelyn esittely-yrityksessä USMF. Jos suoritit menettelyn omien tietojen avulla, rekisterikilville on määritettävä numerosarja. Määritä etikettitulostin, ennen kuin aloitat tämän tehtävän. Valitse Organisaation hallinta > Asetukset > Verkkotulostimet. Valitse toimintoruudussa Asetukset ja valitse sitten Lataa asiakirjan reititysagentin asennusohjelma -painike. Suorita asennusohjelma ja varmista, että toimiva verkkotulostin on määritetty aktiiviseksi, ennen kuin jatkat.


## <a name="set-up-the-gs1-company-prefix"></a>Yrityksen GS1-etuliitteen määrittäminen
1. Valitse Varastonhallinta > Asetukset > Varastonhallinnan parametrit.
2. Syötä yrityksen GS1-etuliite -kenttään GS1-yritysnumeron 7 numeroa.
3. Valitse Tallenna.
4. Sulje sivu.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC-rekisterinumeron järjestyksen määrittäminen
1. Siirry kohtaan Organisaation hallinta > Numerosarjat > Numerosarjat.
2. Valitse Alue-kentässä vaihtoehto.
3. Valitse Viite-kentässä vaihtoehto.
4. Kirjoita arvo Yritys-kenttään.
5. Merkitse valittu rivi luettelossa.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Laajenna Segmentit-osa.
8. Valitse Muokkaa.
9. Valitse Segmentit-taulukon ensimmäinen rivi.
10. Valitse Poista.
11. Valitse Poista.
12. Valitse Tallenna.
13. Sulje sivu.

## <a name="create-the-document-route-layout"></a>Asiakirjan reittiasettelun luominen
1. Valitse Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititysasettelut.
    * Ota SSCC-asettelu käyttöön.  
2. Valitse Uusi.
3. Kirjoita Asettelun tunnus -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Valitse Lisää tekstin loppuun.
7. Valitse Tallenna.
8. Sulje sivu.

## <a name="set-up-the-document-routing"></a>Asiakirjan reitityksen määrittäminen
1. Valitse Varastonhallinta > Asetukset > Asiakirjan reititys > Asiakirjan reititys.
2. Valitse Työtilauksen tyyppi -kentässä vaihtoehto.
3. Valitse Uusi.
4. Kirjoita arvo Varasto-kenttään.
5. Kirjoita arvo Nimi-kenttään.
6. Valitse Uusi.
7. Syötä tai valitse arvo Asettelun tunnus -kenttään.
8. Valitse Nimi-kentästä tulostin, jota haluat käyttää.
9. Valitse Tallenna.
10. Sulje sivu.

## <a name="create-mobile-device-menu"></a>Mobiililaitteen valikon luominen
1. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.
2. Valitse Uusi.
3. Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.
4. Kirjoita Otsikko-kenttään arvo.
5. Valitse Tapa-kentässä vaihtoehto.
6. Valitse Käytä nykyistä työtä -kentässä Kyllä.
7. Valitse Muodosta rekisterikilpi -kentässä Kyllä.
8. Laajenna Työluokat-osa.
9. Valitse Uusi.
10. Kirjoita Työluokan tunnus -kenttään arvo.
11. Valitse Tallenna.
12. Sulje sivu.
13. Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikko.
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Valitse puussa solmu In the tree, select the menu item that you created before.
16. Valitse Muokkaa.
17. Lisää valikkovaihtoehto valikkoon nuolen avulla.
18. Valitse Tallenna.
19. Sulje sivu.

## <a name="update-a-work-template"></a>Työmallin päivittäminen
1. Valitse Varastonhallinta > Asetukset > Työ > Työmallit.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse Muokkaa.
4. Valitse Uusi.
5. Merkitse valittu rivi luettelossa.
6. Valitse Työtyyppi-kentässä Tulosta.
7. Syötä tai valitse arvo Työluokan tunnus -kenttään.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse Siirrä ylöspäin.
10. Valitse Tallenna.
11. Sulje sivu.


