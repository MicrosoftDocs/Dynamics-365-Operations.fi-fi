--- 
title: "Määritä ALV-tunnus"
description: "Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 20f64385b988ff48d865d2d521a9e580dc04c4a2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vat-id"></a>Määritä ALV-tunnus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan. Löydät lisätietoja rekisteröintitunnuksista niiden käsittelystä, mukaan lukien niiden edellytykset, Rekisteröintitunnukset-ohjeaiheesta. 

Nämä tiedot koskevat kaikkia Euroopan maita/alueita. Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa. Tämä tehtävä on tarkoitettu järjestelmänvalvojille. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.

1. Valitse Organisaation hallinto > Yleinen osoitekirja > Rekisteröintityypit > Rekisteröintityypit.
2. Avaa valintaikkuna valitsemalla Uusi.
3. Syötä Nimi-kenttään arvoksi "ALV-tunnus".
4. Kirjoita Kuvaus-kenttään ALV-numero.
5. Syötä tai valitse arvoksi DEU Maa/alue-kentässä
6. Valitse Yksilöllinen-kentässä Kyllä.
    * Valitse tämä valintaruutu varmistaaksesi, että ALV-tunnus on yksilöllinen.  
7. Valitse Ensisijainen maalle -kentässä Kyllä.
    * Valitse tämä valintaruutu, jos ALV-tunnus on voimassa kaikille osoitteille, jotka kuuluvat määritettyyn maahan/alueeseen.  
8. Valitse Luo.
9. ValitseLisää.
10. Syötä tai valitse arvoksi ITA Maa/alue-kentässä.
11. Kirjoita Muoto-kenttään "###########".
    * Kun annat tämäntyyppisen rekisteröintitunnuksen valitulle maalle/alueelle, rekisteröintitunnusta verrataan tähän muotoon.  
12. Valitse Yksilöllinen-valintaruutu.
    * Valitse tämä valintaruutu varmistaaksesi, että ALV-tunnus on yksilöllinen.  
13. Valitse Ensisijainen maalle -valintaruutu.
    * Valitse tämä valintaruutu, jos ALV-tunnus on voimassa kaikille osoitteille, jotka kuuluvat määritettyyn maahan/alueeseen.  
14. Valitse Tallenna.
15. Valitse Organisaation hallinto > Yleinen osoitekirja > Rekisteröintityypit > Rekisteröintiluokat.
16. Valitse Uusi.
17. Syötä tai valitse arvoksi "ALV-tunnus, DEU" Maa/alue-kentässä.
18. Valitse Rekisteröintiluokka-kentän arvoksi "ALV-tunnus".
    * Määritä aiemmin luomasi rekisteröintityyppi esimääritettyyn rekisteröintiluokkaan.  
19. Valitse Uusi.
20. Syötä tai valitse arvoksi "ALV-tunnus, ITA" Maa/alue-kentässä.
21. Valitse Rekisteröintiluokka-kentän arvoksi "ALV-tunnus".
    * Määritä luomasi rekisteröintityyppi esimääritettyyn rekisteröintiluokkaan.  
22. Valitse Tallenna.


