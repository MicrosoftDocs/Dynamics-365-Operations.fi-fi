---
title: Määritä pankin limiitit ja kirjausprofiilit remburssia varten
description: Tässä menettelyssä selvitetään luottokirjeiden käsittelyyn tarvittavan pankkilimiitin ja kirjausprofiilin luonti.
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
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779459"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Määritä pankin limiitit ja kirjausprofiilit remburssia varten

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään luottokirjeiden käsittelyyn tarvittavan pankkilimiitin ja kirjausprofiilin luonti. 

Tässä tehtävässä käytetään USMF-esittely-yritystä.


## <a name="general-ledger-parameter"></a>Kirjanpitoparametri
1. Valitse **Maksuliikenteen hallinta > Asetukset > Maksuliikennetiedot**.
2. Laajenna **Pankkitosite**-osa.
3. Valitse **Ota tuontiremburssi käyttöön** -vaihtoehto.
4. Valitse **Ota vientiremburssi käyttöön** -vaihtoehto.
5. Valitse **Tallenna**.
6. Sulje sivu.

## <a name="create-bank-facility"></a>Luo pankkilimiitti
1. Valitse **Maksuliikenteen hallinta > Asetukset > Pankin limiitit**.
2. Valitse **Uusi**.
3. Anna **Limiittiryhmä**-kenttään pankin limiittiryhmän nimi.
4. Kirjoita **Kuvaus**-kenttään pankin limiittiryhmän kuvaus.
5. Valitse **Tallenna**.
6. Valitse **Limiittityypit**-välilehti.
7. Valitse **Uusi**.
8. Anna **Limiittityyppi**-kenttään yksilöivä koodi.
9. Kirjoita **Kuvaus**-kenttään arvo.
10. Avaa haku napsauttamalla **Limiittiryhmä**-kentässä avattavan valikon painiketta.
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
13. Valitse **Limiitin laatu** -kentästä pankkilimiitin laatu.
14. Valitse **Tallenna**.
15. Sulje sivu.

## <a name="bank-posting-profile"></a>Pankin kirjausprofiili
1. Valitse **Maksuliikenteen hallinta > Asetukset > Pankkitositteiden kirjausprofiili**.
2. Valitse **Uusi**.
3. Avaa haku napsauttamalla **Tilin/ryhmän numero** -kentässä avattavan valikon painiketta.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse tilityksen päätili.
    * Tätä tiliä käytetään laskettaessa kassavirtaennustetta.  
7. Valitse **Veloitustili**-kentässä kulutapahtumien tili.
8. Valitse **Marginaalitili**-kentässä katetapahtumien tili.
    * Tätä tiliä veloitetaan, kun avaava marginaali on kirjattu ja hyvitetään, kun maksu on kirjattu.  
9. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
