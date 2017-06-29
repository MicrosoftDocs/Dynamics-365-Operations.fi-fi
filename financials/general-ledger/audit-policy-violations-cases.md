---
title: "Valvo käytäntövirheitä ja tapauksia"
description: "Tässä artikkelissa kerrotaan, miten valvontatapaukset luodaan valvontakäytäntöjen sääntöjen rikkomuksista. Artikkeli sisältää tietoja myös valvontakäytäntöjen erilaisista tavoista käyttää asiakirjavalinnan päivämääräväliä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 882f99beff256f96b6879c4af4c4ca8a6c4dbec3
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="audit-policy-violations-and-cases"></a>Valvo käytäntövirheitä ja tapauksia

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten valvontatapaukset luodaan valvontakäytäntöjen sääntöjen rikkomuksista. Artikkeli sisältää tietoja myös valvontakäytäntöjen erilaisista tavoista käyttää asiakirjavalinnan päivämääräväliä.

<a name="how-audit-cases-are-generated"></a>Kuinka tarkasteltuja tapauksia luodaan
-----------------------------

Valvontakäytäntöjä käytetään tunnistamaan kuluraportteja, ostotilauksia ja toimittajalaskuja, jotka eivät noudata liiketoimintasääntöjä, jotka määrittelet ja määrität valvontakäytäntösäännöiksi. 

Vavontakäytännöt suoritetaan erätilassa. Valvontakäytäntöä suoritettaessa kaikki käytäntösäännöt, jotka kuuluvat kyseiseen käytäntöön suoritetaan samanaikaisesti.

Kunkin käytäntösääntö käsittelee useita asiakirjoja. Käytäntösääntö valitsee asiakirjoja, jotka ovat asiakirjan valintapäivämäärän alueella ja jotka vastaavat määritettyjä ehtoja. Esimerkiksi yksi käytäntösääntö saattaa valita kuluraportit, joissa on ateriat, jotka ylittävät 50,00. Toinen käytäntösääntö saattaa valita toimittajalaskut, jotka suoritetaan tietylle toimittajalle. Kullekin valitulle asiakirjalle, joka on valittu joukossa, muodostuu rikkominen. Rikkominen on tietue, että tietty asiakirja, kuten lasku 12345, ei seuraa käytäntösääntöä. 

Useita valvontarikkomus tietueita on ryhmitelty ja ne liittyvät valvontatapauksiin. Oletusarvona. kunkin valvontakäytännön tapaukset ryhmitellään valvontakäytäntösäännön perusteella. Halutessasi voit valita muita ryhmittelyehtoja käyttämällä **Tapauksien ryhmittelyehdot** -sivua. Voit ryhmitellä esimerkiksi kulujen otsikot projektitunnuksen mukaan ja toimittajalaskut toimittajatilin mukaan. Tällöin kaikki kuluraportin otsikoiden rikkomiset, joilla on sama projektitunnus, ryhmitellään samaan tapaukseen ja kaikki toimittajalaskut, joilla on sama toimittajatili, ryhmitellään samaan tapaukseen. 

> [!NOTE]
> Valvontakäytännön säännöt, jotka perustuvat **Duplikaatti**-kyselytyyppiin, rikkeitä ei ole ryhmitelty käytäntösäännöittäin tai ehtojen mukaan, jotka on määritetty **Tapausten ryhmittelyehto** -sivulla. Sen sijaan ryhmittelyperusteena ovat kriteerit, jotka sisältyvät tarkistuskäytännön sääntöön. Esimerkiksi, jos käytäntösääntö laskee kuluraporttien kaksoiskappaleiden kulut samalle summalle, myyjän tunnukselle ja päivämäärälle, kaikki kulut, joilla on samat arvot niissä kentissä, ovat yksi tapaus. Kulut, joilla on erilaiset arvot, ovat erillisessä laatikossa.

Sen jälkeen kun valvontatapaukset on luotu, kun ne käsitellään käyttämällä tyypillisiä prosesseja tapaushallinnan avulla.

## <a name="document-selection-date-ranges"></a>Asiakirjojen valinnan päivämäärävälit
Kun tarkistuskäytäntö suoritetaan, kukin käytäntösääntö valitsee tietyntyyppiset asiakirjat, joiden päivämäärä on asiakirjan valitulla päivämäärävälillä. Asiakirjan valinnan päivämääräväli määritetään **Lisäasetukset**-sivulla. Useisiin asiakirjoihin on liitetty useampi kuin yksi päivä. Päivämääräkenttä, jota tarkistuskäytäntösääntö käyttää täsmennetään **Käytäntösääntötyyppi**-sivulla.

Tässä on muita tapoja, joilla tarkistuskäytäntö käyttää asiakirjan valinnan päivämääräväliä:

-   Menettely käyttää jokaisen käytäntösäännön sitä versiota, joka on voimassa asiakirjan valinnan päivämäärävälin viimeisenä päivänä. Voit tarkastella kunkin käytäntösäännön voimassaolopäivämääriä **Valvontakäytännöt**-luettelosivulla.
-   Käytäntösääntöä käyttää oraganisaation solmuja, jotka liittyvät käytäntöön viimeisenä päivänä asiakirjan valinnan päivämäärävälin aikana. Vain ne organisaatiosolmut, jotka liittyvät käytäntöön nykyisin näkyvät **Valvontakäytännöt**-luettelosivulla.
-   Käytäntösäännöt, jotka perustuvat **Luettelohaku**-kyselylajiin, käytäntö käsittelee valvottuja asiakirjoja, jotka ovat voimassa asiakirjan valitun ajanjakson viimeisenä päivänä.


Lisätietoja on kohdassa [Tilintarkastuskäytännön säännöt](audit-policy-rules.md)




