---
title: Ylläpidon käyttökatko
description: Tässä ohjeaiheessa kuvataan ylläpidon käyttökatkoja resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918241"
---
# <a name="maintenance-downtime"></a>Ylläpidon käyttökatko


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Voit luoda huoltoseisokkien rekisteröintejä työtilauksessa valitulle käyttöomaisuudelle. Tästä on hyötyä, jos haluat rekisteröidä huoltoseisokit yhdelle tai useammalle tuotantoalueen koneelle. Ensin luodaan huoltoseisokkien syykoodit, joita haluat käyttää, esimerkiksi erittely ja suunniteltu pysähdys. Tämä tehdään kohdassa **Ylläpidon käyttökatkon syykoodit**. Seuraavaksi voit luoda kunnossapitoseisokkeja koskevia rekisteröintejä **Ylläpidon käyttökatko** -kohdassa ja lisätä tarvittavat syykoodit.

## <a name="create-maintenance-downtime-reason-codes"></a>Kunnossapitoseisokkien syykoodien luominen

1. Valitse **Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Ylläpidon käyttökatkon syykoodit**.

2. Valitse **Uusi**.

3. Lisää tunnus **Ylläpidon käyttökatkon syykoodi** -kenttään.

4. Kirjoita **Nimi**-kenttään syykoodin nimi.

5. Valitse **KPI, sisällytä** -valintaruutu, jos syykoodi sisällytetään käyttöomaisuuden KPI-laskelmiin. Suunniteltuja tuotanto pysähdyksiä ei yleensä sisällytetä KPI-laskelmiin, koska ne eivät vaikuta odotettuun suorituskykyyn.

6. Valitse **Tallenna**.

![Kuva 1](media/15-work-orders.png)


Kun olet luonut huoltoseisokkien syykoodit, joita haluat käyttää, voit luoda työtilauksille ja käyttöomaisuudelle kunnossapitoseisokkimerkintöjä.


## <a name="create-maintenance-downtime-registrations"></a>Kunnossapitoseisokkien reskiteröintien luominen

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus ja valitse **Ylläpidon käyttökatko**.

3. Valitse **Uusi**.

4. Lisää huoltoseisokkien rekisteröimisen päivämäärä ja aika **Alkaen**- ja **Asti**-kenttiin.

5. Kun poistut **Asti**-kentästä, kesto tunteina lisätään automaattisesti **Kesto**-kenttään.

6. Valitse syykoodi **Ylläpidon käyttökatkon syykoodi** -kentässä.

7. Toista vaiheet 3-6, jos haluat lisätä uusia rekisteröintejä.

8. Valitse **Tallenna**.


![Kuva 2](media/16-work-orders.png)


Ylläpitoseisokkien rekisteröintien laskennassa käytettävä kalenteri määräytyy resurssi- ja parametriasetusten valinnan mukaan. Jos resurssi on valittuna resurssille kohdassa **Kaikki resurssit** > **Käyttöomaisuus-** pikavälilehden **Resurssi**-kentässä, käytetään liittyvän resurssiryhmän kalenteria, joka näkyy seuraavassa kuvassa.

![Kuva 3](media/17-work-orders.png)


Jos käyttöomaisuudelle ei ole valittu resurssia, käytetään **Resurssienhallinnan parametrit** -kohdassa valittua vakiokalenteria seuraavassa kuvassa esitetyllä tavalla.

![Kuva 4](media/18-work-orders.png)


Näet yhteenvedon kaikista käyttökatkorekisteröinneistä valitsemalla **Yrityksen resurssien hallinta** > **Kyselyt** > **Ylläpidon käyttökatko**.

>[!NOTE]
>Kaikki **Resurssien hallinta** -moduulissa käytettävät kalenterit määritetään kohdassa **Organisaation hallinto** > **Asetukset** > **Kalenterit** > **Kalenterit**.

