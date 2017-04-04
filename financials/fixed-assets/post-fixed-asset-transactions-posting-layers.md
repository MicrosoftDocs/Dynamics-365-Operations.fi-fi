---
title: "Kirjaa käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin"
description: "Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Kirjaa käyttöomaisuustapahtumien kirjaaminen kirjanpitotasoihin

Tässä artikkelissa on yleiskuvaus käyttöomaisuustapahtumien kirjanpitotason toiminnosta.

Käyttöomaisuus poistetaan yleensä eri tavoin eri tarkoituksissa. Verotuksessa poisto lasketaan nykyisillä verosäännöillä, jotta poisto ennen veroja on suurin mahdollinen, mutta raportoinnissa poisto lasketaan kirjanpitolakien ja -standardien mukaisesti. Erilaiset poistot lasketaan ja kirjataan kirjaustasoille erikseen.

Kullekin käyttöomaisuuteen liitetylle kirjalle on määritetty tietty kirjanpitotaso, jolla on yleinen poistotavoite. Kirjanpitotasoja on kymmenen: Nykyinen, Liiketoiminnot, Vero ja seitsemän mukautettua tasoa Kirjanpitokirjaukset voi poistaa käytöstä asettamalla Kirjaa kirjanpitoon -kentän arvoksi Ei. Kirjanpitotaso -kenttään määritetään automaattisesti Ei. Yleensä käytetään veroraportointia kirjat, joita ei kirjata pääkirjanpitoon. Tämä lähestymistapa Lisää lisää joustavuutta historiallisia tapahtumia käyttöomaisuuskirjan, koska niitä ei ole vahvistettu kirjanpitoon.

Käyttöomaisuuden kirjauskansiot määritetään Kirjauskansionimet sivulla kohdassa kirjanpito > kirjauskansion asetukset > kirjauskansionimet. Kukin kirjauskansio, johon poistoja voi kirjata, määritetään vain yhdelle kirjaustasolle sen kirjauskansionimen mukaan. Kirjauskansion kirjaustasoa ei voi muuttaa. Tämän rajoituksen avulla varmistetaan, että kunkin kirjanpitotason tapahtumat säilytetään erillään. Kullekin kirjaustasolle on luotava vähintään yksi kirjauskansionimi. Jos käytät kirjat, joita ei kirjata kirjanpitoon, on myös luotava päiväkirja, jossa Kirjaustaso määrittää ei mitään.

Voit määrittää kirjanpitotilejä käyttöomaisuustapahtumille Käyttöomaisuuserän kirjausprofiili -sivulla. Valitse kullekin kirjausprofiilille asianmukainen tapahtumatyyppi ja kirja ja määritä sitten kirjanpitotilit. Määritä kirjausprofiilin tietue erikseen jokaiselle kirjalle, joka kirjataan kirjanpitoon.

> [!NOTE] 
> Johdettu kirjojen avulla voit kirjata tapahtumia eri kirjaustasoille samaan aikaan. Ensisijaisen kirjan tapahtumat luodaan kirjauskansioon, jonka kirjaustaso vastaa kirjan kirjaustasoa. Kirjauksen aikana johdetun kirjan tapahtumat kirjataan asianmukaisille kirjaustasoille.

Lisätietoja saat [kirjat on saatu](derived-books.md) ja [kirjaaminen johdettujen kirjoja](post-derived-value-models.md).


