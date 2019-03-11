---
title: Prosessien tehtävät
description: Tässä ohjeaiheessa on tietoja erityyppisistä tehtävistä, joita voidaan käyttää työhönottoprosessissa.
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2019
ms.locfileid: "374754"
---
# <a name="activities-in-the-hiring-processes"></a>Työhönottoprosessien tehtävät

[!include[banner](../includes/banner.md)]

Tehtävät voidaan lisätä työhönottoprosessin osaksi Microsoft Dynamics 365 for Talent: Attractissa. Tehtävät voidaan lisätä prosessimalliin, tai ne voidaan lisätä suoraan työn työhönottoprosessiin. Työn määrittämisen jälkeen valitaan prosessimalli, jonka jälkeen malliin sisältyvät tehtävät liitetään työhön. Jos mallia ei ole valittu, käytetään oletusmallia. Työhönottoprosessia voidaan muokata työn osalta myös mallin liittämisen jälkeen.

> [!NOTE] 
> Prosessimallit sisältyvät kattavaan työhönottolaajennukseen.

## <a name="prospect-activity"></a>Potentiaalinen ehdokas -tehtävä

Potentiaalinen ehdokas -tehtävä määrittää, voidaanko potentiaaliset ehdokkaat lisätä työhön. Potentiaaliset ehdokkaat voidaan oletusarvoisesti lisätä työhön. Voit poistaa Potentiaalinen ehdokas -tehtävän käytöstä valitsemalla **Ota potentiaaliset ehdokkaat käyttöön** -asetukseksi **Ei käytössä**. Kun Potentiaalinen ehdokas -tehtävä on otettu käyttöön, rekrytointipäälliköt voivat lisätä ja tarkastella potentiaalisia ehdokkaita työn kohdalla näkyvässä **Potentiaalinen ehdokas** -välilehdessä.

## <a name="application-activity"></a>Hakemus-tehtävä

Työhönottoprosessimallissa on oltava Hakemus-tehtävä. Jos haluat lähettää sähköpostia ehdokkaille, kun lähettävät hakemuksen tai kun heidät lisätään Hakemus-vaiheeseen, valitse **Lähetä viesti ehdokkaalle** -asetukseksi **Käytössä**.

## <a name="interview-schedule-and-feedback-activity"></a>Haastattelujen aikataulu- ja palautetehtävä

Tässä tehtävässä on kolme osaa: Ehdokkaan käytettävyystietojen pyytäminen, Aikataulu ja Palaute. Käytä työmallin haastattelutehtävää, jos haluat sisällyttää ehdokkaan käytettävyystietojen pyytämisen, aikataulun ja palautteen prosessin osaksi sen sijaan, että käyttäisit niitä työhönottoprosessin erillisinä osina. Lisätietoja on kohdassa [Haastattelujen aikataulutus ja palaute](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>PowerApps-tehtävä

PowerApps-tehtävän avulla voi upottaa Microsoft PowerApps -sovelluksen työhönottoprosessiin. Sovellus voi olla pakollinen kaikille hakijoille, vain sisäisille hakijoille, vain ulkoisille hakijoille tai ei millekään hakijoille. Jos sovellus on merkitty pakolliseksi, sen on oltava valmis, ennen kuin vaiheessa voi edetä. Jos sovellusta ei ole merkitty pakolliseksi, tehtävä on valinnainen vaihe ja vaiheessa voidaan siirtyä, vaikka sovellus ei olisi valmis.

Jos haluat tallentaa PowerApps-tehtävän työhönottoprosessiin, sinun on annetta PowerApps-tunnus. Voit etsiä PowerApps-tunnuksen valitsemalla ensin [PowerApps](https://web.powerapps.com), sitten **Sovellukset** ja lopuksi **Tiedot**.

Jos valitset asetuksen, joka **sallii osallistujien lisäämisen tehtävään**, PowerApps-tehtävää käyttävään sovellukseen voidaan lisätä osallistujia. Esimerkki: Organisaatio on luonut PowerApps-sovelluksen, joka teknisten tehtävien haastattelukysymyksistä koostuva kirjasto. Organisaatio on nyt palkkaamassa uutta ohjelmistokehittäjää ja on lisännyt PowerApps-tehtävän ohjelmistokehittäjäroolin työhönottoprosessiin. Jos asetus, joka **sallii osallistujien lisäämisen tehtävään**, on valittu, hakijaa ohjelmistokehittäjän rooliin harkitseva rekrytoija tai rekrytointipäällikkö voi lisätä henkilöitä PowerApps-tehtävään. Kyseiset henkilöt voivat sitten tarkastella haastattelukysymykset sisältävää sovellusta.

> [!NOTE]
> PowerApps-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.

## <a name="youtube-activity"></a>YouTube-tehtävä

Voit jakaa YouTube-tehtävässä YouTube-videon työhönottoprosessin osana. Jos haluat tallentaa YouTube-tehtävän työhönottoprosessiin, sinun on määritettävä YouTube-videon URL-osoite. Voit sallia osallistujien lisäämiseen tehtävään samoin kuin PowerApps-tehtävässä. Jos valitset **Näytä vain ehdokas** -asetuksen, video näytetään vain ehdokaskokemuksen osana. Sitä ei näytetä Attractin työhönottoprosessissa.

> [!NOTE]
> YouTube-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.

## <a name="web-content-activity"></a>Internet-sisältö-tehtävä

Internet-sisältö-tehtävässä voit upottaa verkkosisältöä työhönottoprosessiin. Jos haluat tallentaa Internet-sisältö-tehtävän työhönottoprosessiin, sinun on määritettävä sisällön URL-osoite. Voit sallia osallistujien lisäämiseen tehtävään samoin kuin PowerApps- ja YouTube-tehtävissä. Jos valitset **Näytä vain ehdokas** -asetuksen, sisältö näytetään vain ehdokaskokemuksen osana. Sitä ei näytetä Attractin työhönottoprosessissa. Voit valita näytettävän sisällön koon.

> [!NOTE]
> Internet-sisältö-tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.

## <a name="microsoft-forms-activity"></a>Microsoft Forms -tehtävä

Microsoft Forms -tehtävän avulla voi upottaa Microsoft Forms -lomakkeen työhönottoprosessiin. Voit luoda Microsoft Formsin avulla tietovisoja ja erilaisia kyselyjä. Jos haluat tallentaa Microsoft Forms -tehtävän työhönottoprosessiin, sinun on määritettävä lomakkeen URL-osoite. Voit sallia osallistujien lisäämiseen tehtävään samoin kuin PowerApps-, YouTube- ja Internet-sisältö-tehtävissä. Jos valitset **Näytä vain ehdokas** -asetuksen, lomake näytetään vain ehdokaskokemuksen osana. Sitä ei näytetä Attractin työhönottoprosessissa.

Tekijät voivat muuttaa Microsoft Formsissa asetuksia siten, että organisaation ulkopuoliset käyttäjät voivat vastata kyselyyn tai tietovisaan. Siinä tapauksessa käyttäjät lähettävät vastaukset anonyymisti. Jos haluat nähdä, kuka on vastannut kyselyyn tai tietovisaan, voit edellyttää, että vastaajat ilmoittavat nimensä kyselyn tai tietovisan osana.

> [!NOTE]
> Microsoft Forms -tehtävää voi käyttää vain kattavan työhönottolaajennuksen kanssa.
