---
title: Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten
description: Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bfdef0cd535f47bb1df9fb7494043d3dd519c5b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779877"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten

[!include [banner](../../includes/banner.md)]

Tämä tehtävä pankkilimiitin ja kirjausprofiilin, joita tarvitaan takausasiakirjan käsittelemiseen.



Tässä tehtävässä käytetään esittely-yritystä USMF. 




## <a name="general-ledger-parameter"></a>Kirjanpitoparametri
1. Valitse **Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot**.
2. Laajenna **Pankkitosite**-osa.
3. Valitse **Ota takausasiakirja käyttöön** -vaihtoehto.
4. Avaa haku napsauttamalla **Tapahtumakirjauskansio**-kentässä avattavan valikon painiketta.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse **Numerojärjestykset**-välilehti.
    * Määritä takausasiakirjan numeron ja takausasiakirjan tapahtumaviitteiden numerosarjakoodi  
8. Valitse **Tallenna**.
9. Sulje sivu.

## <a name="create-bank-facility"></a>Luo pankkilimiitti
1. Valitse **Maksuliikenteen hallinta > Asetukset > Pankin limiitit**.
2. Valitse **Uusi**.
3. Kirjoita **Limiittiryhmä**-kenttään takausasiakirjatapahtuman pankin limiittiryhmän nimi.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Tallenna**.
6. Valitse **Limiittityypit**-välilehti.
7. Valitse **Uusi**.
8. Kirjoita **Limiittityyppi**-kenttään pankin limiittisopimukseen liittyvä pankin limiittityyppi.
9. Kirjoita **Kuvaus**-kenttään arvo.
10. Avaa haku napsauttamalla **Limiittiryhmä**-kentässä avattavan valikon painiketta.
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse **Limiitin laatu -kentässä vaihtoehto.
14. Valitse **Tallenna**.
15. Sulje sivu.

## <a name="bank-posting-profile"></a>Pankin kirjausprofiili
1. Valitse **Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili**.
2. Valitse **Uusi**.
3. Avaa haku napsauttamalla **Tilin/ryhmän numero** -kentässä avattavan valikon painiketta.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse **Selvitystili**-kentässä päätili tilitystä varten.
7. Valitse **Veloitustili**-kentässä kulutapahtumien tili.
8. Valitse **Katetili**-kentästä katetapahtumien tili.
9. Valitse **Selvitystili**-kentässä takausasiakirjatapahtuman selvitystili. 
10. Valitse **Tallenna**.
11. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
