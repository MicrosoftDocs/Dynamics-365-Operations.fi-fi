---
title: Määritä edun oikeutussäännöt ja -käytännöt
description: Tässä tallenteessa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "859226"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Määritä edun oikeutussäännöt ja -käytännöt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tallenteessa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin.  

Tämän tallenteen luomisessa käytetty demotietojen yritys on USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Etukelpoisuuden käytäntösääntötyypin luominen
1. Valitse Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytäntösääntötyypit.
2. Valitse Uusi.
3. Kirjoita arvo Säännön nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Kyselyn nimi -kentässä avattavan valikon painike.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Valitse Tallenna.
8. Sulje sivu.

## <a name="benefit-eligibility-policy"></a>Etukelpoisuuden käytäntö
1. Valitse Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytännöt.
2. Valitse aiemmin luotu etukäytäntö.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Ota käyttöön Käytäntöorganisaatiot-osien laajennus.  Tässä voit lisätä organisaatiot, jotka haluat lisätä käytäntöön, tai poistaa niitä.
5. Laajenna tai tiivistä Käytäntösäännöt-osa.
6. Valitse luettelosta aiemmin luotu käytäntösääntö.
7. Valitse Luo käytäntösääntö.
8. Syötä Voimaantulopäivä-kenttään päivämäärä, jolloin haluat ottaa käytännön käyttöön.
    * Kun voimaantulo- ja päättymispäivät määritetään, voit muuttaa käytäntösääntöjä jatkossa. Näin käytäntöön ei tarvitse palata silloin, kun haluat ottaa muutokset käyttöön.  
9. 
    * Jos esimerkiksi haluat kohdistaa säännön vain myyntipäällikköihin, voit luoda seuraavan Where-lauseen: kun toimen kuvaus on yhtä suuri kuin myyntipäällikkö.  Where-lauseita voi yhdistää säännössä And- ja Or-operaattorin avulla.  
10. Valitse OK.
11. Sulje sivu.
12. Sulje sivu.

## <a name="assign-rule-to-benefit"></a>Säännön liittäminen etuun
1. Siirry kohtaan Henkilöstöhallinto > Edut > Edut.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Laajenna tai tiivistä Oikeutussäännöt-osa.
5. Valitse Muokkaa.
6. Valitse Oikeutus-kentässä luettelosta Sääntöön perustuva -kohta.
7. Avaa haku valitsemalla Sääntötyyppi-kentässä avattavan valikon painike.
8. Etsi ja valitse luettelosta aiemmin luotu sääntö.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Valitse Tallenna.
11. Sulje lomake.

