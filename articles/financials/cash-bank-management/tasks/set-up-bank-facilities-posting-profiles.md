---
title: Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten
description: Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f696f5aa809692a0cc2c4ff559945a301480d7e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "321659"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.



Tässä tehtävässä käytetään esittely-yritystä USMF. 




## <a name="general-ledger-parameter"></a>Kirjanpitoparametri
1. Valitse Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot.
2. Laajenna Pankkitosite-osa.
3. Valitse Ota takausasiakirja käyttöön -vaihtoehto.
4. Avaa haku napsauttamalla Tapahtumakirjauskansio-kentässä avattavan valikon painiketta.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse Numerojärjestykset-välilehti.
    * Määritä takausasiakirjan numeron ja takausasiakirjan tapahtumaviitteiden numerosarjakoodi  
8. Valitse Tallenna.
9. Sulje sivu.

## <a name="create-bank-facility"></a>Luo pankkilimiitti
1. Valitse Maksuliikenteen hallinta > Asetukset > Pankin limiitit.
2. Valitse Uusi.
3. Kirjoita Limiittiryhmä-kenttään takausasiakirjatapahtuman pankin limiittiryhmän nimi.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Tallenna.
6. Valitse Limiittityypit-välilehti.
7. Valitse Uusi.
8. Kirjoita Limiittityyppi-kenttään pankin limiittisopimukseen liittyvä pankin limiittityyppi.
9. Kirjoita Kuvaus-kenttään arvo.
10. Avaa haku napsauttamalla Limiittiryhmä-kentässä avattavan valikon painiketta.
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse Limiitin laatu -kentässä vaihtoehto.
14. Valitse Tallenna.
15. Sulje sivu.

## <a name="bank-posting-profile"></a>Pankin kirjausprofiili
1. Valitse Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili.
2. Valitse Uusi.
3. Avaa haku napsauttamalla Tilin/ryhmän numero -kentässä avattavan valikon painiketta.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse Selvitystili-kentässä päätili tilitystä varten.
7. Valitse Veloitustili-kentästä kulutapahtumien tili.
8. Valitse Marginaalitili-kentästä katetapahtumien tili.
9. Valitse Selvitystili-kentässä takausasiakirjatapahtuman selvitystili. 
10. Valitse Tallenna.
11. Sulje sivu.

