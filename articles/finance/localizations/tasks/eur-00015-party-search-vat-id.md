---
title: EUR-00015 Osaouolen haku ALV-tunnuksen avulla
description: Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
ms.openlocfilehash: 0688de30327abe0925efe3daf44bcbab8a096c97
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288473"
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
