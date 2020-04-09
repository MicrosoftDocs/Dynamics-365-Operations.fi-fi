---
title: Toimittajan mallien välillä siirtyminen
description: Tässä aiheessa käsitellään kuinka vaihtaa toimittajan tietojen integrointia Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173036"
---
# <a name="switch-between-vendor-designs"></a>Toimittajan mallien välillä siirtyminen

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Toimittajatietojen virta 

Jos päätät käyttää **Tili**-yksikköä, kun haluat tallentaa **Organisaatio**-tyypin ja **Yhteyshenkilö**-yksikön **Henkilö**-tyypin myymälätoimittajia, määritä seuraavat työnkulut. Muussa tapauksessa tätä kokoonpanoa ei tarvita.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille

**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit. Kullekin mallille luodaan työnkulku.

+ Toimittajien luonti Tilit-yksikössä
+ Toimittajien luonti toimittajat-yksikössä
+ Toimittajien päivittäminen Tilit-yksikössä
+ Toimittajien päivittäminen toimittajat-yksikössä

Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:

1. Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Luo toimittajia tiliyksikössä** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan luontiskenaarion.

    ![Toimittajien luonti Tilit-yksikön työnkulkuprosessissa](media/create_process.png)

2. Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Päivitä toimittajia tiliyksikössä** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Tilli**-yksikön toimittajan päivitysskenaarion.
3. Luo uusi työnkulkuprosessi **Tili**-yksikölle ja valitse **Luo toimittajia toimittajayksikössä** -työnkulun prosessimalli.
4. Luo uusi työnkulkuprosessi **Tili**-yksikölle ja valitse **Päivitä toimittajia toimittajayksikössä** -työnkulun prosessimalli.
5. Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi. Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. Aktivoi **Tili**- ja **Toimittaja**-yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Tili**-yksikköä **Organisaatio**-tyyppisten toimittajien tietojen tallentamiseen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille

**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit. Kullekin mallille luodaan työnkulku.

+ Luo henkilötyyppisiä toimittajia toimittajayksikköön
+ Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikköön
+ Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikköön
+ Päivitä henkilötyyppisiä toimittajia toimittajayksikköön

Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:

1. Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan luontiskenaarion.
2. Luo uusi työnkulkuprosessi **Toimittaja**-yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Yhteyshenkilö**-yksikön toimittajan päivitysskenaarion.
3. Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Luo henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.
4. Luo uusi työnkulkuprosessi **Yhteyshenkilö**-yksikölle ja valitse **Päivitä henkilötyyppisiä toimittajia yhteyshenkilöyksikössä** -työnkulun prosessimalli.
5. Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi. Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.
6. Aktivoi **Yhteyshenkilö**- ja **Toimittaja**-yksiköissä luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö**-yksikköä **Henkilö**-tyyppisten toimittajien tietojen tallentamiseen.
