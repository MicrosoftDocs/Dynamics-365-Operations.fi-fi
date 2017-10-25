---
title: "Yleisen osoitekirjan ja lisäosoitekirjojen määrittämissuunnitelma"
description: "Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin yleinen osoitekirja ja lisäosoitekirjat määritetään. Jotkin päätökset vaativat tuotteen muilla alueilla, esimerkiksi organisaatiohierarkiassa, tehtyjen päätösten vahvistamisen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>Yleisen osoitekirjan ja lisäosoitekirjojen määrittämissuunnitelma

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin Microsoft Dynamics 365 for Finance and Operationsin yleinen osoitekirja ja lisäosoitekirjat määritetään. Jotkin päätökset vaativat tuotteen muilla alueilla, esimerkiksi organisaatiohierarkiassa, tehtyjen päätösten vahvistamisen.

<a name="global-address-book"></a>Yleinen osoitekirja
-------------------

Ennen kuin aloita yleisen osoitekirjan käsittelyn, sille on määritettävä oletusarvot. Näitä oletusarvoja käytetään sitten mahdollisissa lisäosoitekirjoissa, jotka luot. 

**Päätökset:**

-   Missä järjestyksessä nimet näytetään **Henkilö**-tyypin osapuolitietueissa? Yksi järjestys on esimerkiksi sukunimi, toinen nimi, etunimi.
-   Poistetaanko osapuolitietueet osoitekirjasta, kun roolitietue poistetaan? Jos esimerkiksi asiakastietue poistetaan, poistetaanko myös osapuolitietue?
-   Ilmoitetaanko käyttäjille uutta tietuetta luotaessa, jos yleisestä osoitekirjasta löytyy tietueen kaksoiskappale?
-   Sisällytetäänkö DUNS (Data Universal Numbering System) -numero osapuolitietueen tietoihin?
-   Jos DUNS-numero sisällytetään osapuolitietueeseen, tarkistetaanko, että numero on yksilöllinen?
-   Kun yleiseen osoitekirjaan luodaan osapuolitietue, haluatko oletusosapuolen tyypin, henkilön vai organisaation?
-   Mitkä käyttäjäroolit saavat osapuolitietueiden yksityisten osoitteiden ja yhteystietojen käyttöoikeudet?

## <a name="additional-address-books"></a>Lisäosoitekirjat
Kun olet luonut yleisen osoitekirjan, voit luoda tarvittavia lisäosoitekirjoja, kuten oman osoitekirjan organisaation kullekin yritykselle tai toimialalle. Fabrikam on esimerkiksi kansainvälinen organisaatio, jolla on useita yrityksiä ja toimialoja. Fabrikam suunnittelee toimialakohtaisten osoitekirjojen luontia. Fabrikam suunnittelee useassa toimipaikassa toimiville toimialoille, kuten paineilmatyökalujen toimiala, oman osoitekirjan luontia kullekin toimipaikalle. Fabrikamin IT-päällikkö Chris on luonut seuraavan luettelon tarvittavista osoitekirjoista. Tässä luettelossa on myös kuvaus osapuolitietueista, joiden on sisällyttävä kuhunkin osoitekirjaan.

-   **Julkisen sektorin sopimukset (PubSC)** – kaikkien Fabrikamin julkisen sektorin sopimusten osapuolien osapuolitietueet.
-   **Yksityisen sektorin sopimukset (PriSC)** – kaikkien Fabrikamin yksityisen sektorin sopimusten osapuolien osapuolitietueet.
-   **Sähköiset työkalut (ET)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat sähköisten työkalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen sähköisten työkalujen parissa.
-   **Paineilmatyökalut (PTJPN)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.
-   **Paineilmatyökalut (PTUSA)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-US-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.

**Päätös:**

-   Kuinka monta lisäosoitekirjaa luot?

### <a name="address-book-security"></a>Osoitekirjan suojaus

Voit luoda osoitekirjoja koska tahansa ja voit myös määrittää osoitekirjojen suojauksen parametrit koska tahansa. Sinun ei tarvitse määrittää osoitekirjan suojausoikeuksia, mutta jos et tee niin, organisaation kaikki työntekijät voivat tarkastella kaikkia kyseisen osoitekirjan osapuolitietueita. Voit määrittää osapuolitietueiden suojausoikeudet osoitekirjojen kautta. Suojausoikeudet perustuvat ryhmiin. Näin taataan, että vain siihen ryhmään määritetyt työntekijät, joilla on osoitekirjan käyttöoikeus, voivat tarkastella kyseisen osoitekirjan osapuolitietueita. Sinun on valittava ryhmät, joilla on kunkin osoitekirjan käyttöoikeudet. Määritä kullekin osoitekirjalle suojausoikeudet, jotka sallivat käytön tietyille ryhmille tai estävät käytön. Kun myönnät ryhmälle osoitekirjan käyttöoikeuden, kyseisen ryhmän kaikki jäsenet voivat tarkastella osoitekirjan tietueita. Jos et myönnä ryhmälle osoitekirjan käyttöoikeutta, kyseisen ryhmän jäsenet eivät voivat tarkastella osoitekirjaa tai sen sisältöä. 

**Päätös:**

-   Mitkä ryhmät saavat kunkin luomasi uuden osoitekirjan käyttöoikeudet?




