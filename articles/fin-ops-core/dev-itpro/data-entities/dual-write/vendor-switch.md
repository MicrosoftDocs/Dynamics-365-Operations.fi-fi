---
title: Toimittajan mallien välillä siirtyminen
description: Tässä aiheessa käsitellään kuinka vaihtaa toimittajan tietojen integrointia Finance and Operations -sovellusten ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750591"
---
# <a name="switch-between-vendor-designs"></a>Toimittajan mallien välillä siirtyminen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Toimittajatietojen virta 

Jos päätät käyttää **Tili**-taulua, kun haluat tallentaa **Organisaatio**-tyypin ja **Yhteyshenkilö**-taulun **Henkilö**-tyypin myymälätoimittajia, määritä seuraavat työnkulut. Muussa tapauksessa tätä kokoonpanoa ei tarvita.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Käytä laajennettua toimittajan rakennetta organisaatiotyypin toimittajille

**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit. Kullekin mallille luodaan työnkulku.

+ Toimittajien luonti Tilit-taulussa
+ Toimittajien luonti Toimittajat-taulussa
+ Toimittajien päivitys Tilit-taulussa
+ Toimittajien päivitys Toimittajat-taulussa

Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:

1. Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Luo toimittajia Tilit-taulussa** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Tilli**-taulun toimittajan luontiskenaarion.

    ![Toimittajien luonti Tilit-taulun työnkulkuprosessissa](media/create_process.png)

2. Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Päivitä toimittajia Tilit-taulussa** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Tili**-taulun toimittajan päivitysskenaarion.
3. Luo uusi työnkulkuprosessi **Tili**-taululle ja valitse **Luo toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.
4. Luo uusi työnkulkuprosessi **Tili**-taululle ja valitse **Päivitä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.
5. Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi. Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.

    ![Muunna taustatyönkuluksi -painike](media/background_workflow.png)

6. Aktivoi **Tili**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Tili**-taulua **Organisaatio**-tyyppisten toimittajien tietojen tallentamiseen.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Käytä laajennettua toimittajan rakennetta henkilötyypin toimittajille

**Dynamics365FinanceExtended**-ratkaisupaketti sisältää seuraavat työnkulkuprosessin mallit. Kullekin mallille luodaan työnkulku.

+ Luo henkilötyyppisiä toimittajia Toimittajat-taulussa
+ Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
+ Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa
+ Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa

Noudata näitä vaiheita, kun haluat luoda uusia työnkulkuprosesseja työnkulun prosessimallien avulla:

1. Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Luo henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Yhteyshenkilö**-taulun toimittajan luontiskenaarion.
2. Luo uusi työnkulkuprosessi **Toimittaja**-taululle ja valitse **Päivitä henkilötyyppisiä toimittajia Yhteyshenkilöt-taulussa** -työnkulun prosessimalli. Valitse sitten **OK**. Tämä työnkulku käsittelee **Yhteyshenkilö**-taulun toimittajan päivitysskenaarion.
3. Luo uusi työnkulkuprosessi **Yhteyshenkilö**-taululle ja valitse **Luo henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.
4. Luo uusi työnkulkuprosessi **Yhteyshenkilö**-taululle ja valitse **Päivitä henkilötyyppisiä toimittajia Toimittajat-taulussa** -työnkulun prosessimalli.
5. Voit määrittää työnkulut vaatimuksistasi riippuen joko reaaliaikaisiksi työnkuluiksi tai taustatyönkuluiksi. Jos haluat määrittää työnkulun taustatyönkuluksi, valitse **Muunna taustatyönkuluksi**.
6. Aktivoi **Yhteyshenkilö**- ja **Toimittaja**-tauluissa luodut työnkulut, jotta voit alkaa käyttää **Yhteyshenkilö**-taulua **Henkilö**-tyyppisten toimittajien tietojen tallentamiseen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]