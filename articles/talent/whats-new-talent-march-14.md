---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. maaliskuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c3beef9ef4e73eaf76f861735bb154fa630703f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023904"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (14. maaliskuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä ohjelmakorjauksia.

## <a name="changes-in-onboarding"></a>Onboardingin muutokset
Tässä julkaisussa on vähäisiä ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
**Koontiversio 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Suorituskyvyn hallinta ei toimi kaikissa tilanteissa, kun käytetään päällekkäisiä käyttöoikeusrooleja.
Muutokset tässä versiossa mahdollistavat suorituskyvyn hallinnan skenaariot käytettäessä valmiita tai monistettuja rooleja.

### <a name="mass-assign-checklists-to-workers"></a>Tarkistusluetteloiden määrittäminen työntekijöille joukkotoimintona
Tämän muutoksen ansiosta voit valita useita työntekijöitä ja joukkomäärittää yhden tai useamman tarkistusluettelon näille työntekijöille. 

### <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operationsin käyttöympäristöpäivitys 24
Lisätietoja Finance and Operationsin käyttöympäristöpäivitys 24:stä on kohdassa [Finance and Operations -käyttöympäristöpäivitys 24:n uudet ja muuttuneet ominaisuudet (maaliskuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Platform 24:n merkittävät muutokset ovat esimerkiksi seuraavat: 

- Hälytykset ovat käytettävissä Talentissa.
- Päivitetty siirtymispalkki on nyt yhtenäinen toimiston otsikon kanssa.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Toimiston sijainnin päivitys siirtää kontekstin työntekijäluettelon alkuun
Nykyinen version avulla, toimiston sijainnin muuttaminen ei enää muuta sen työntekijän kontekstia, jota tarkastelet, kun määrität toimiston sijaintia.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Toimen päättymispäivämäärä ei näy oikein työntekijän palkkauksen ja siirron toiminnoissa
Toimen päättymispäivät näkyvät nyt oikein perustuen käyttäjän ensisijaiseen aikavyöhykkeeseen toimintoja käytettäessä.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service -työentiteetti ei salli Työlaji- ja Työtehtävä-kenttien päivittämistä
Common Data Service -entiteetit synkronoituvat nyt oikein päivitettäessä Common Data Servicea käyttäen.

## <a name="coming-soon"></a>Tulossa pian

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)
Monissa yrityksissä etuuspäälliköillä on ehkä vain määrättyjen kompensaatiotietueiden käyttöoikeus. Ne voivat olla johtajille tai alueellisille työntekijöille. Tämä muutoksen ansiosta henkilöstöhallinto voi hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Voit määrittää suojausrooleja kiinteille ja muuttuville suunnitelmille, jotka määrittelevät suunnitelmien ja suunnitelmiin liittyvien työntekijöiden tietojen, kuten palkan tai bonustietojen, käytön. Näille työntekijöille maksettavia korvauksia voi käsitellä vain roolit, joille on myönnetty käyttöoikeus.

###  <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Finance and Operations -käyttöympäristöpäivitys 24:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköposti-ilmoituksia yhteyshenkilöille, kun tapahtuma käynnistyy.

### <a name="duplicate-employee-check-interface-changes"></a>Työntekijätietojen kaksoiskappaleiden tarkistus: Käyttöliittymän muutokset
Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.
