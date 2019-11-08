---
title: Ylläpidon käyttökatko
description: Tässä ohjeaiheessa kuvataan ylläpidon käyttökatkoja resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad9f1b2a0e63b4fb0d6daceb451c3a1dc1ec7de7
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626148"
---
# <a name="maintenance-downtime"></a>Ylläpidon käyttökatko

[!include [banner](../../includes/banner.md)]


Voit luoda ylläpidon käyttökatkojen rekisteröintejä työtilauksessa valitulle resurssille. Tästä on hyötyä, jos haluat rekisteröidä ylläpidon käyttökatkoja yhdelle tai useammalle tuotantoalueen koneelle. Ensin luodaan ylläpidon käyttökatkon syykoodit, joita haluat käyttää, kuten **Erittely** ja **Suunniteltu pysäytys**. Tämä tehdään sivulla **Ylläpidon käyttökatkon syykoodit**. Seuraavaksi voit luoda kunnossapitoseisokkeja koskevia rekisteröintejä **Ylläpidon käyttökatko** -sivulla ja lisätä tarvittavat ylläpidon käyttökatkon syykoodit.

## <a name="create-maintenance-downtime-reason-codes"></a>Kunnossapitoseisokkien syykoodien luominen

1. Valitse **Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Ylläpidon käyttökatkon syykoodit**.

2. Valitse **Uusi**.

3. Syötä **Ylläpidon käyttökatkon syykoodi** -kenttään tunnus ylläpidon käyttökatkon syykoodille.

4. Anna nimi **Nimi**-kenttään.

5. Valitse **KPI, sisällytä** -valintaruutu, jos syykoodi on tarkoitus ottaa huomioon resurssin suorituskykyilmaisimien (KPI) laskennassa. Yleisesti ottaen suunniteltuja tuotantokatkoja ei pitäisi sisällyttää KPI-laskelmiin, koska ne eivät vaikuta odotettuun suorituskykyyn.

6. Valitse **Tallenna**.

Alla olevassa kuvassa on esimerkki **Ylläpidon käyttökatkon syykoodit** -sivusta.

![Kuva 1](media/15-work-orders.png)

Kun olet luonut ylläpidon käyttökatkon syykoodit, joita haluat käyttää, voit luoda työtilauksille ja käyttöomaisuudelle ylläpidon käyttökatkorekisteröintejä.


## <a name="create-maintenance-downtime-registrations"></a>Kunnossapitoseisokkien reskiteröintien luominen

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta ja sitten toimintoruudun **Työtilaus**-välilehden **Resurssi**-ryhmässä **Ylläpidon käyttökatko**.

3. Valitse **Uusi**.

4. Lisää ylläpidon käyttökatkojen rekisteröinnin päivämäärä- ja aikaväli kenttiin **Alkaen** ja **Asti**.

>[!NOTE]
>Kun poistut **Asti**-kentästä, kesto tunteina lisätään automaattisesti **Kesto**-kenttään.

5. Valitse syykoodi **Ylläpidon käyttökatkon syykoodi** -kentässä.

6. Voit lisätä rekisteröintejä toistamalla kohtien 3–5 toimet.

7. Valitse **Tallenna**.

Alla olevassa kuvassa näkyy esimerkki ylläpidon käyttökatkon rekisteröinnistä.

![Kuva 2](media/16-work-orders.png)

Ylläpidon käyttökatkojen rekisteröintien laskennassa käytettävä kalenteri määräytyy resurssi- ja parametriasetusten valinnan mukaan. Jos resurssi on valittuna resurssille **Kaikki resurssit** -sivun **Käyttöomaisuus**-pikavälilehden **Resurssi**-kentässä, käytetään liittyvän resurssiryhmän kalenteria, joka näkyy seuraavassa kuvassa.

![Kuva 3](media/17-work-orders.png)

Jos käyttöomaisuudelle ei ole valittu resurssia, käytetään **Resurssienhallinnan parametrit** -sivulla valittua vakiokalenteria seuraavassa kuvassa esitetyllä tavalla.

![Kuva 4](media/18-work-orders.png)

Näet yhteenvedon kaikista ylläpidon käyttökatkojen rekisteröinneistä valitsemalla **Resurssienhallinta** > **Kyselyt** > **Ylläpidon käyttökatko**.

>[!NOTE]
>Kaikki **Resurssien hallinta** -moduulissa käytettävät kalenterit määritetään kohdassa **Organisaation hallinto** > **Asetukset** > **Kalenterit** > **Kalenterit**.

