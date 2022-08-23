---
title: EUR-00015 Toimittajan ALV-tunnuksen rekisteröinti
description: Tässä toimintaohjeessa kuvataan, miten ALV-tunnukset ja verovapausnumerot lisätään toimittajan tilille.
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
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
ms.openlocfilehash: ce5d2a11e1576b772a91bc58d1d7ad330e8c7481
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273748"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a>EUR-00015 Toimittajan ALV-tunnuksen rekisteröinti

[!include [banner](../../includes/banner.md)]

Tässä toimintaohjeessa kuvataan, miten ALV-tunnukset ja verovapausnumerot lisätään toimittajan tilille. Tämä prosessi on samanlainen yrityksille ja asiakkaille. 

Ennen kuin tämän menettelyn voi suorittaa, ALV-tunnukset on määritettävä. Tämä menettely koskee kaikkia Euroopan maita/alueita. Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa. Nämä toimet tekee yleensä tietojen hallinnan järjestelmänvalvoja, ostoreskontrapäällikkö tai myyntireskontrapäällikkö. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

1. Siirry kohtaan Ostoreskontra > Toimittajat > Kaikki toimittajat.
2. Etsi luettelosta asiakas DE-01001 ja valitse se.
3. Valitse Rekisteröintitunnukset.
4. ValitseLisää.
5. Valitse ALV-tunnus.
6. Kirjoita Rekisteröintinumero-kenttään arvo.
    * Määritä valitun toimittajan saksalainen ALV-tunnus. Tunnuksen on vastattava rekisteröintityypille määritettyä muotoa.  
7. Valitse Yleiset-välilehti.
8. Kirjoita päivämäärä Voimassa-kenttään.
9. Valitse Tallenna.
10. Valitse Uusi.
11. Kirjoita Nimi tai kuvaus -kenttään arvo.
    * Syötä arvoksi esimerkiksi ITA.  
12. Syötä tai valitse arvo Maa/alue-kentässä.
    * Voit valita esimerkiksi arvon ITA.  
13. Valitse Ensisijainen maalle -kentässä Kyllä.
14. Valitse Tallenna.
15. Valitse Yhteenveto-välilehti.
16. ValitseLisää.
17. Syötä tai valitse arvo Rekisteröintityyppi-kentässä.
    * Valitse esimerkiksi ALV-tunnus.  
18. Kirjoita Rekisteröintinumero-kenttään arvo.
    * Määritä esimerkiksi italialainen ALV-tunnus.  Tunnuksen on vastattava rekisteröintityypille määritettyä muotoa.  
19. Valitse Tallenna.
20. Sulje sivu.
21. Etsi haluamasi tietue luettelosta ja valitse se.
    * Voit valita esimerkiksi arvon DE-01001  
22. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
23. Laajenna Lasku ja toimitus -osa.
24. Valitse Muokkaa.
25. Anna tai valitse Verovapausnumero-kentässä arvo.
26. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
