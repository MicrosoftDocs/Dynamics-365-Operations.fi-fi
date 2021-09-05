---
title: Etuuskelpoisuussääntöjen ja -käytäntöjen määrittäminen
description: Tässä aiheessa käsitellään edun oikeutussääntöjen ja -käytäntöjen luomisesta sekä sääntöjen määrittämistä etuihin.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 59a0ee2f8a1411e921da1d348b87038f9aafccd3
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416854"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Etuuskelpoisuussääntöjen ja -käytäntöjen määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa käsitellään edun oikeutussääntöjen ja -käytäntöjen luomisesta sekä sääntöjen määrittämistä etuihin.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Etukelpoisuuden käytäntösääntötyypin luominen

1. Valitse **Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytäntösääntötyypit**.
2. Valitse **Uusi**.
3. Anna **Säännön nimi** -kenttään arvo.
4. Anna arvo **Kuvaus**-kentässä.
5. Avaa haku valitsemalla **Kyselyn nimi** -kentässä avattavan valikon painike.
6. Valitse luettelossa valitulla rivillä oleva linkki.
7. Valitse **Tallenna**.
8. Sulje sivu.

## <a name="benefit-eligibility-policy"></a>Etukelpoisuuden käytäntö

1. Valitse **Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytännöt**.
2. Valitse aiemmin luotu etukäytäntö.
3. Valitse luettelossa valitulla rivillä oleva linkki.
4. Ota käyttöön **Käytäntöorganisaatiot**-osien laajennus. Voit lisätä organisaatiot, jotka haluat lisätä käytäntöön, tai poistaa niitä.
5. Laajenna tai tiivistä **Käytäntösäännöt**-osa.
6. Valitse luettelosta aiemmin luotu käytäntösääntö.
7. Valitse **Luo käytäntösääntö**.
8. Syötä **Voimaantulopäivä**-kenttään päivämäärä, jolloin haluat ottaa käytännön käyttöön.
    * Kun voimaantulo- ja päättymispäivät määritetään, voit muuttaa käytäntösääntöjä jatkossa. Näin käytäntöön ei tarvitse palata silloin, kun haluat ottaa muutokset käyttöön.  
9. Lisää tarvittaessa where-lauseke **Lisää ehto** -kenttään.
    * Jos esimerkiksi haluat kohdistaa säännön vain myyntipäällikköihin, voit luoda seuraavan where-lauseen: kun toimen kuvaus on yhtä suuri kuin myyntipäällikkö. Useita where-lauseita voi lisätä säännössä kerralla.  
10. Valitse **OK**.
11. Sulje sivu.

## <a name="assign-rule-to-benefit"></a>Säännön liittäminen etuun

1. Siirry kohtaan **Henkilöstöhallinto > Edut > Edut**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse luettelossa valitulla rivillä oleva linkki.
4. Laajenna tai tiivistä **Oikeutussäännöt**-osa.
5. Valitse **Muokkaa**.
6. Valitse **Oikeutus**-kentässä sääntö.
7. Valitse **Sääntötyyppi**-kentässä aiemmin luotu sääntö.
9. Valitse luettelossa valitulla rivillä oleva linkki.
10. Valitse **Tallenna**.
11. Sulje lomake.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
