---
title: Käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin
description: Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770709"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta.

Käyttöomaisuus poistetaan yleensä eri tavoin eri tarkoituksissa. Verotuksessa poisto lasketaan nykyisillä verosäännöillä, jotta poisto ennen veroja on suurin mahdollinen, mutta raportoinnissa poisto lasketaan kirjanpitolakien ja -standardien mukaisesti. Erilaiset poistot lasketaan ja kirjataan kirjaustasoille erikseen.

Kullekin käyttöomaisuuteen liitetylle kirjalle on määritetty tietty kirjanpitotaso, jolla on yleinen poistotavoite. Kirjanpitotasoja on kymmenen: Nykyinen, Liiketoiminnot, Vero ja seitsemän mukautettua tasoa Kirjanpitokirjaukset voi poistaa käytöstä asettamalla Kirjaa kirjanpitoon -kentän arvoksi Ei. Kirjanpitotaso -kenttään määritetään automaattisesti Ei. Kirjoja, joita ei kirjata pääkirjanpitoon, käytetään yleensä veroraportoinnissa. Tämän ansiosta voit poistaa menneitä tapahtumia käyttöomaisuuskirjasta, koska niitä ei ole vahvistettu kirjanpitoon.

Käyttöomaisuuden kirjauskansiot määritetään Kirjauskansionimet sivulla kohdassa kirjanpito > kirjauskansion asetukset > kirjauskansionimet. Kukin kirjauskansio, johon poistoja voi kirjata, määritetään vain yhdelle kirjaustasolle sen kirjauskansionimen mukaan. Kirjauskansion kirjanpitotasoa ei voi muuttaa. Tämän rajoituksen avulla varmistetaan, että kunkin kirjanpitotason tapahtumat säilytetään erillään. Kullekin kirjaustasolle on luotava vähintään yksi kirjauskansionimi. Jos käytät kirjoja, joita ei kirjata kirjanpitoon, sinun on luotava kirjauskansio, jossa kirjanpitotasoksi on määritetty Ei mitään.

Voit määrittää kirjanpitotilejä käyttöomaisuustapahtumille Käyttöomaisuuserän kirjausprofiili -sivulla. Valitse kullekin kirjausprofiilille asianmukainen tapahtumatyyppi ja kirja ja määritä sitten kirjanpitotilit. Määritä kirjausprofiilin tietue erikseen jokaiselle kirjalle, joka kirjataan kirjanpitoon.

> [!NOTE] 
> Käyttämällä johdettuja arvomalleja voit kirjata tapahtumia eri kirjaustasoille samalla kertaa. Ensisijaisen kirjan tapahtumat luodaan kirjauskansioon, jonka kirjaustaso vastaa kirjan kirjaustasoa. Kirjauksen aikana johdetun kirjan tapahtumat kirjataan asianmukaisille kirjaustasoille.

Lisätietoja on kohdassa [Johdetut kirjat](derived-books.md) ja [Kirjaaminen johdettujen kirjojen avulla](post-derived-value-models.md).



