---
title: Yleisen osoitekirjan ja lisäosoitekirjojen suunnitelma
description: Tässä ohjeaiheessa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin yleinen osoitekirja ja lisäosoitekirjat määritetään.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f0a53e1f9b378759e0c5adbe0612a5fa8cddc82
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796943"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Yleisen osoitekirjan ja muiden osoitekirjojen suunnitteleminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, millaiset asiat pitää ottaa huomioon ja millaisia päätöksiä pitää tehdä suunnitteluprosessin aikana, ennen kuin yleinen osoitekirja ja lisäosoitekirjat määritetään. Jotkin päätökset vaativat tuotteen muilla alueilla, esimerkiksi organisaatiohierarkiassa, tehtyjen päätösten vahvistamisen.

## <a name="global-address-book"></a>Yleinen osoitekirja

Ennen kuin aloita yleisen osoitekirjan käsittelyn, sille on määritettävä oletusarvot. Näitä oletusarvoja käytetään sitten mahdollisissa lisäosoitekirjoissa, jotka luot.

**Päätökset**

- Missä järjestyksessä nimet näytetään **Henkilö**-tyypin osapuolitietueissa? Yksi järjestys on esimerkiksi sukunimi, toinen nimi, etunimi.
- Poistetaanko osapuolitietueet osoitekirjasta, kun roolitietue poistetaan? Jos esimerkiksi asiakastietue poistetaan, poistetaanko myös osapuolitietue?
- Ilmoitetaanko käyttäjille uutta tietuetta luotaessa, jos yleisestä osoitekirjasta löytyy tietueen kaksoiskappale?
- Sisällytetäänkö DUNS (Data Universal Numbering System) -numero osapuolitietueen tietoihin?
- Jos DUNS-numero sisällytetään osapuolitietueeseen, tarkistetaanko, että numero on yksilöllinen?
- Kun yleiseen osoitekirjaan luodaan osapuolitietue, haluatko oletusosapuolen tyypin, henkilön vai organisaation?
- Mitkä käyttäjäroolit saavat osapuolitietueiden yksityisten osoitteiden ja yhteystietojen käyttöoikeudet?

## <a name="additional-address-books"></a>Lisäosoitekirjat

Kun olet luonut yleisen osoitekirjan, voit luoda tarvittavia lisäosoitekirjoja, kuten oman osoitekirjan organisaation kullekin yritykselle tai toimialalle. Fabrikam on esimerkiksi kansainvälinen organisaatio, jolla on useita yrityksiä ja toimialoja. Fabrikam suunnittelee toimialakohtaisten osoitekirjojen luontia. Fabrikam suunnittelee useassa toimipaikassa toimiville toimialoille, kuten paineilmatyökalujen toimiala, oman osoitekirjan luontia kullekin toimipaikalle. Fabrikamin IT-päällikkö Chris on luonut seuraavan luettelon tarvittavista osoitekirjoista. Tässä luettelossa on kuvaus osapuolitietueista, joiden on sisällyttävä kuhunkin osoitekirjaan.

- **Julkisen sektorin sopimukset (PubSC)** – kaikkien Fabrikamin julkisen sektorin sopimusten osapuolien osapuolitietueet.
- **Yksityisen sektorin sopimukset (PriSC)** – kaikkien Fabrikamin yksityisen sektorin sopimusten osapuolien osapuolitietueet.
- **Sähköiset työkalut (ET)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat sähköisten työkalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen sähköisten työkalujen parissa.
- **Paineilmatyökalut (PTJPN)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-Japan-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.
- **Paineilmatyökalut (PTUSA)** – kaikkien niiden osapuolien osapuolitietueet, jotka osallistuvat paineilmatyökalujen ostoon tai myyntiin tai jotka toimivat muutoin Fabrikamin Fabrikam-US-yrityksen toimittamien tai sille ostettujen paineilmatyökalujen parissa.

**Päätös:**

- Kuinka monta lisäosoitekirjaa luot?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]