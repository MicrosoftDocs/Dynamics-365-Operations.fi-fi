---
title: EUR-00015 Osaouolen haku ALV-tunnuksen avulla
description: Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b112d37dace0e43c5171f746a60bf987ae77c3aa65edc515f93b53d4e1cf625
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758754"
---
# <a name="eur-00015-party-search-using-vat-id"></a>EUR-00015 Osaouolen haku ALV-tunnuksen avulla

[!include [banner](../../includes/banner.md)]

Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella. Ennen kuin suoritat nämä toimet, ALV-tunnukset on määritettävä ja toimittajien, asiakkaiden ja yritysten ALV-tunnukset on syötettävä järjestelmään.

Tämä menettely koskee kaikkia Euroopan maita/alueita. Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa. Nämä toimet tekee yleensä ostoreskontrapäällikkö tai myyntireskontrapäällikkö. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

1. Valitse Organisaation hallinto > Yleinen osoitekirja > Yleinen osoitekirja.
2. Valitse Rekisteröintitunnuksen haku.
3. ValitseLisää.
4. Syötä tai valitse arvo Rekisteröintityyppi-kentässä.
    * Jos esimerkiksi haluat löytää osapuolet, joiden rekisteröintitunnus on tyyppiä ALV-tunnus, valitse ALV-tunnus.  
5. Syötä tai valitse arvo Maa/alue-kentässä.
    * Syötä arvoksi esimerkiksi DEU.  
6. Kirjoita Rekisteröintinumero-kenttään arvo.
7. Valitse Etsi.
    * Kaikki osapuolet, joilla on kyseinen rekisteröintitunnus näytetään.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]