---
title: Raportin tuoterakenteet valmiiksi
description: "Tässä artikkelissa on tietoja tuoterakenteiden ilmoittamisesta valmiiksi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 318c88f88277a8300b1fcda5056a9a92c9a81eae
ms.lasthandoff: 03/31/2017


---

# <a name="report-boms-as-finished"></a>Raportin tuoterakenteet valmiiksi

Tässä artikkelissa on tietoja tuoterakenteiden ilmoittamisesta valmiiksi.

**Ilmoita valmiiksi**- ja **Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivuilta voi ilmoittaa tuoterakenteet valmiiksi. Käsitteellisesti tuoterakenteen valmiiksi ilmoittamisen prosessi on sama kuin tuotantotilauksen valmiiksi ilmoittamisen prosessi. Tätä prosessia voi käyttää esimerkiksi yksinkertaisissa kokoonpano- ja varusteluprosesseissa, joissa tuotantotilausten edistyneitä ominaisuuksia ei tarvita. Voit ilmoittaa **Ilmoita valmiiksi** -sivulla useita tuoterakenteita valmiiksi yhtenä eränä. **Max. raportti valmiiksi** -sivulla voit vain yhden Tuoterakenteen ilmoittaminen valmiiksi yhdellä kertaa. **Valmiiksi** sivu on käytettävissä Varastonhallinta-valikon vaihtoehtoa, ja molemmat sivut ovat saatavilla valikon nimikkeet **tuotteiden julkaissut** sivulle.

## <a name="report-as-finished-page"></a>Ilmoita valmiiksi -sivu
Jos avaat **Ilmoita valmiiksi **-sivun vapautetusta tuotteesta, sivu ehdottaa, että valmiiksi ilmoitetaan vakiovaraston oletusmäärä. Aktiivinen tuoterakenneversio näytetään oletusarvoisesti, mutta voit vaihtaa toiseen tuoterakenneversioon, jos valittavana on muita hyväksyttyjä versioita. Voit myös poistaa sivulla tietueita ja luoda vapautetuille tuotteille uusia, valmiiksi ilmoitettavia tietueita. Jos haluat käyttää kyselyä tuotteen valitsemiseen, valitse valikossa **Valitse**. Voit vahvistaa valittujen tuotteiden raportoinnin manuaalisesti valmiiksi valitsemalla **OK**. Vaihtoehtoisesti voit myös määrittää prosessin suoritettavaksi eränä. Kun valmiiksi ilmoittamisprosessi on vahvistettu, järjestelmä luo tuoterakennekirjauskansion, jossa varastoon kirjaaminen käsitellään. Kirjauskansiossa on yksi rivinimike valmiille tuotteelle ja yksi rivinimike kullekin tuoterakenneriville. Voit määrittää, tehdään kirjaus kirjauskansioon automaattisesti vai jätetäänkö se avoimeksi oikaisuja varten.

## <a name="max-report-as-finished-page"></a>Maks. Ilmoita valmiiksi sivun
**Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivulla kukin tuoterakennerivi ilmaisee tuotteen valmiiksi ilmoitettavan kappalemäärän. Tämä laskelma perustuu kunkin materiaalirivin fyysiseen käytettävissä olevaan varastoon. Seuraavassa esimerkissä yksi nimiketunnus FG kuluttaa kaksi kappaletta raaka-ainetta RM10 ja yhden kappaleen raaka-ainetta RM20. Koska käytettävissä olevassa varastossa on vain 10 kappaletta raaka-ainetta RM10, nimikettä FG voidaan ilmoittaa valmiiksi enintään viisi kappaletta. Tämä arvo näkyy **Ilmoita valmiiksi -kirjausten enimmäismäärä** -kentässä.

| Tasaa | Nimiketunnus | Määrä | Varastosaldo | Maks. Ilmoita valmiiksi |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Tuoterakenteet, joissa on useita tasoja
Kun tuoterakenteessa on useita tasoja, voit hallita materiaalien laskentaa kaikilla tasoilla käyttämällä **Hajotus**-kenttää. Tämä kenttä on sekä **Ilmoita valmiiksi**- että **Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivulla. Valittavissa ovat seuraavat vaihtoehdot:

-   **Ei koskaan** – perustana olevia tuoterakenteita ei hajoteta, jos materiaalista on puute.
-   **Aina** – Kaikki perustana olevat tuoterakenteet hajotetaan kokonaan. Niinpä puolivalmiiden komponenttinimikkeiden vapaata käytettävissä olevaa varastoa ei käytetä.
-   **Puute** – pohjana olevat tuoterakenteet hajotetaan vain, jos tarvittava materiaalimäärää ei ole kokonaan saatavissa.

### <a name="example"></a>Esimerkki

Tässä esimerkissä lopputuotetta (nimiketunnus FG) on valmiina kolme kappaletta, jotka voidaan ilmoittaa valmiiksi. Tässä kuvassa on kaksitasoinen tuoterakenne.

| Tasaa | Nimiketunnus | Tuoterakennerivin määrä | Varastosaldo |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Seuraavissa tauluissa näytetään, miten **Hajotus**-kentän asetus vaikuttaa tuoterakenteen kirjauskansiorivit luontitapaan. **Hajotus: ei koskaan**

| Tasaa | Nimiketunnus | Määrä |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Edellisessä taulukossa näkyy vain nimikenumeroa COMP pidetään vähennetään kirjauskansiossa. Päiväkirjan riville nimikenumeron RM, joka on osa COMP, ei ole leikattu ja COMP kaksi varasto-osat eivät ole huomioon. **Hajotus: aina**

| Tasaa | Nimiketunnus | Määrä |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

Tässä tapauksessa nimiketunnus COMP on hajotettu raaka-aineeseen, nimiketunnukseen RM. Kahta varastossa käytettävissä olevaa COMP-kappaletta ei oteta huomioon kulutettavana RM-määränä. **Hajotus: puute**

| Tasaa | Nimiketunnus | Määrä |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

Tässä tapauksessa kaksi varastossa käytettävissä olevaa kappaletta nimiketunnusta COMP otetaan huomioon. Koska kuitenkin tarvitaan kolme kappaletta nimiketunnusta FG, tarvitaan myös yksi kappale nimiketunnusta RM, jotta lisäkappale nimiketunnusta COMP voidaan valmistaa.


