---
title: Kohdista maksuaikataulu laskukirjauskansioon
description: Tässä aiheessa kuvataan, kuinka maksu lisätään toimittajan laskukirjauskansioon.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075567"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Kohdista maksuaikataulu laskukirjauskansioon

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Finance -versiossa 10.0.25 toimittajalaskukirjauskansio tukee nyt maksusuunnitelmaa.

Tämän toiminnon käyttäminen on mahdollista, kun ominaisuudenhallinnassa on käytössä **Kohdista maksuaikataulu laskukirjauskansioon** -toiminto.

Kun ominaisuus on otettu käyttöön, **Laskukirjauskansio**-sivulle lisätään uusi **Maksusuunnitelma**-kenttä. Kun luot laskukirjauskansion rivin, jos toimittajan maksuehtoja ylläpidetään ja maksuehdot valitaan maksusuunnitelmasta, **Maksusuunnitelma**-kenttä päivitetään **Laskukirjauskansio**-sivulla.

Voit muuttaa käytettyä maksusuunnitelmaa liiketoimintatarpeiden mukaan. Toimittajan laskukirjauskansion kirjauksen aikana luodaan toimittajan avoimia tapahtumia maksusuunnitelman mukaisesti.

Voit tarkastella useita maksusuunnitelmasta luotuja toimittajan avoimia tapahtumia kohdassa **Ostoreskontra \> Laskut \> Avoimet toimittajan laskut** antamalla laskunumeron tai toimittajatilin.

Voit tarkistaa tai konfiguroida maksusuunnitelmaa kohdassa **Ostoreskontra \> Maksun asetukset \> Maksusuunnitelma**.

Voit määrittää maksuehdot ja määrittää maksusuunnitelman kohdassa **Ostoreskontra \> Maksun asetukset \> Maksuehdot**.

Jos haluat ylläpitää toimittajan maksuehtoja, siirry kohtaan **Ostoreskontra \> Kaikki toimittajat**, valitse toimittajatili ja määritä sitten **Maksu**-välilehdessä **Maksuehdot**-kenttä.

Maksusuunnitelmatoiminto on myös käytettävissä **Toimittajan laskurekisteri** -prosessissa. Jos laskurekisterin kirjauskansiossa on valittu maksusuunnitelma, useita toimittajan maksurivejä **ei** luoda laskurekisterin kirjaamisen yhteydessä. Toimittajan maksurivit luodaan, kun lasku hyväksytään.

## <a name="limitation"></a>Rajoitus

Jos maksusuunnitelma on laskun otsikossa odottavassa toimittajalaskussa, siinä on lisäsivu, jonka avulla käyttäjät voivat muokata maksurivejä. (Käyttäjät voivat esimerkiksi muokata kunkin maksurivin eräpäivää ja arvoa.) Laskukirjauskansiosta muodostetuilla maksuriveillä on maksusuunnitelman arvo.

Nämä toiminnot ovat käytettävissä toimittajan laskukirjauskansiossa ja odottavissa laskuissa tulevassa versiossa.
