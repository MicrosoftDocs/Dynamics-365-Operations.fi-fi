---
title: Tuoterakenteiden valmiiksi raportoiminen
description: "Tässä artikkelissa on tietoja tuoterakenteiden valmiiksi raportoimisesta."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cf96f16c8388e8e91025412d95e4d5c091b9ecc8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="report-boms-as-finished"></a>Tuoterakenteiden valmiiksi raportoiminen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja tuoterakenteiden valmiiksi raportoimisesta.

**Ilmoita valmiiksi**- ja **Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivuilta voi ilmoittaa tuoterakenteet valmiiksi. Käsitteellisesti tuoterakenteen valmiiksi ilmoittamisen prosessi on sama kuin tuotantotilauksen valmiiksi ilmoittamisen prosessi. Tätä prosessia voi käyttää esimerkiksi yksinkertaisissa kokoonpano- ja varusteluprosesseissa, joissa tuotantotilausten edistyneitä ominaisuuksia ei tarvita. Voit ilmoittaa **Ilmoita valmiiksi** -sivulla useita tuoterakenteita valmiiksi yhtenä eränä. Voit ilmoittaa **Ilmoita valmiiksi -kirjausten enimmäismäärä** -sivulla kerralla valmiiksi vain yhden tuoterakenteen. **Ilmoita valmiiksi** -sivun voi valita Inventoinnin- ja varastonhallinta -valikosta. Molemmat sivut voi valita **Vapautetut tuotteet** -sivun valikosta.

## <a name="report-as-finished-page"></a>Ilmoita valmiiksi -sivu
Jos avaat **Ilmoita valmiiksi**-sivun vapautetusta tuotteesta, sivu ehdottaa, että valmiiksi ilmoitetaan vakiovaraston oletusmäärä. Aktiivinen tuoterakenneversio näytetään oletusarvoisesti, mutta voit vaihtaa toiseen tuoterakenneversioon, jos valittavana on muita hyväksyttyjä versioita. Voit myös poistaa sivulla tietueita ja luoda vapautetuille tuotteille uusia, valmiiksi ilmoitettavia tietueita. Jos haluat käyttää kyselyä tuotteen valitsemiseen, valitse valikossa **Valitse**. Voit vahvistaa valittujen tuotteiden raportoinnin manuaalisesti valmiiksi valitsemalla **OK**. Vaihtoehtoisesti voit myös määrittää prosessin suoritettavaksi eränä. Kun valmiiksi ilmoittamisprosessi on vahvistettu, järjestelmä luo tuoterakennekirjauskansion, jossa varastoon kirjaaminen käsitellään. Kirjauskansiossa on yksi rivinimike valmiille tuotteelle ja yksi rivinimike kullekin tuoterakenneriville. Voit määrittää, tehdään kirjaus kirjauskansioon automaattisesti vai jätetäänkö se avoimeksi oikaisuja varten.

## <a name="max-report-as-finished-page"></a>Maks. ilmoita valmiiksi -sivu
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

Edellisessä taulussa nähtiin, miten vain nimiketunnus COMP katsotaan vähennetyksi kirjauskansiossa. COMP-tunnukseen kuuluvaa nimiketunnusta RM ei hajoteta kirjauskansion riville eikä kahta varastossa käsillä olevaa COMP-kappaletta oteta huomioon. **Hajotus: aina**

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




