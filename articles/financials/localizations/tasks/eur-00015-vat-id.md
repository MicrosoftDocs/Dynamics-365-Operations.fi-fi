---
title: EUR-00015 ALV-tunnuksen määrittäminen
description: Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b22c3e15a9d7b228ec724ca77a61a18b11b257
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537856"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 ALV-tunnuksen määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä toimintosarja opastaa ALV-tunnuksen rekisteröinnin edellytykset, kuten rekisteröintityypin määrittämisen ja sen liittämisen rekisteröintiluokkaan. Löydät lisätietoja rekisteröintitunnuksista niiden käsittelystä, mukaan lukien niiden edellytykset, Rekisteröintitunnukset-ohjeaiheesta. 

Nämä tiedot koskevat kaikkia Euroopan maita/alueita. Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa. Tämä tehtävä on tarkoitettu järjestelmänvalvojille. Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

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

