---
title: Luo ostosopimus
description: Tämä menettely opastaa luomaan ostosopimuksen.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547626"
---
# <a name="create-a-purchase-agreement"></a>Luo ostosopimus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely opastaa luomaan ostosopimuksen. Se on yleensä ostopäällikön tehtävä. Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi. Ennen aloittamista on määritettävä ostosopimusluokitukset. Kun olet luonut sopimuksen, voit luoda sen avulla ostotilauksen, jolloin ostotilauksen ehdot kopioituvat otsikkoon ja niille tilauksen riveille, joihin sopimus vaikuttaa.


## <a name="create-a-new-purchase-agreement"></a>Luo uusi ostosopimus
1. Valitse Hankinta > Ostosopimukset > Ostosopimukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku napsauttamalla Ostosopimuksen luokitus -kentässä avattavan valikon painiketta.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Laajenna Yleiset-osa.
10. Kirjoita päivämäärä Vanhentumispäivä-kenttään.
    * Tämä vanhentumispäivä on kaikkien sitoutumisrivien oletusarvo ja määrittää, miten kauan kukin sitoutuminen on voimassa.  
11. Kirjoita Asiakirjan nimi -kenttään ostosopimuksen nimi.
    * Jätä Oletussitoumus -kentän arvoksi Tuotteen määrän vahvistus (tai vaihda tarvittaessa tähän arvoon).  
    * Sitoutumisen oletusavo määrittää sopimusrivien vaihtoehdot. Jos tarvitset sopimuksen rivejä luodessasi uuden sitoutumistyypin, sinun on muutettava otsikon oletussitoutumista.  Sitoutumistyyppejä on 4: Tuotteen määrän vahvistus – koskee tiettyä tuotemäärää. Tuotteen arvon vahvistus – koskee tuotteen tiettyä valuuttasumma. Tuoteluokan arvon sitoutuminen – koskee tiettyä hankintaluokan valuuttasummaa, jossa summa voi olla luettelonimike tai ei-luettelonimike. Arvon sitoutuminen – koskee tiettyä valuuttasumma, jonka voi täyttää mikä tahansa tuote tai hankintaluokka.  
12. Valitse OK.

## <a name="add-a-commitment"></a>Lisää sitoutuminen
1. Valitse Lisää rivi.
2. Merkitse valittu rivi luettelossa.
3. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
4. Valitse tuote,johon haluat lisätä sitoutumisen.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Kirjoita numero Määrä-kenttään.
    * Kokonaismäärä, jonka olet sopinut ostavasi toimittajalta.  
7. Syötä Yksikköhinta-kenttään numero.
8. Laajenna Rivin erittely -osa.
9. Valitse Maksimi pakotetaan -asetukseksi Kyllä.
    * Maksimi pakotetaan -vaihtoehto rajoittaa sitoutumisen käyttöä. Voit ostaa enintään rivin Määrä-kentässä määritetyn määrän.  
10. Tiivistä Rivitiedot-osa.

## <a name="add-header-conditions"></a>Lisää otsikkoehdot
1. Valitse toimintoruudussa Asetukset.
2. Valitse Vaihda näkymä.
3. Valitse Otsikkonäkymä.
4. Laajenna Ehdot-osa.
5. Avaa haku valitsemalla Maksutapa-kentässä avattavan valikon painike.
    * Toimittajatilin maksuehdot näkyvät tässä oletusarvoisesti.       
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku napsauttamalla Toimitustapa-kentässä avattavan valikon painiketta.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Avaa haku napsauttamalla Toimitusehdot-kentässä avattavan valikon painiketta.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="confirm-and-activate-the-agreement"></a>Vahvista ja aktivoi sopimus
1. Valitse toimintoruudussa Ostosopimus.
2. Valitse Vahvistus.
    * Valitse Merkitse sopimus voimassa olevaksi -asetukseksi Kyllä.  
3. Valitse OK.
4. Valitse toimintoruudussa Ostosopimus.
5. Valitse Ostosopimuksen vahvistukset.
    * Esikatselu/tulostus-vaihtoehdolla voi luoda ostosopimusasiakirjan, jonka voi tulostaa tai lähettää asiakkaalle. Jos päivität sopimusta myöhemmin ja vahvistat sen uudelleen, molemmat versiot näkyvät tässä.  
6. Sulje sivu.

