---
title: Ylläpitoaikataulu
description: Tässä ohjeaiheessa kerrotaan ylläpitoaikataulusta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89938a4c5fd9a520c6582215a438670f73085228
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252939"
---
# <a name="maintenance-schedule"></a>Ylläpitoaikataulu

[!include [banner](../../includes/banner.md)]

 

Huoltoaikataulu sisältää luettelon kaikista odotetuista ennaltaehkäisevistä huoltosuunnitelmista, huoltopyynnöistä ja huoltokierroksista. Jotkin aikataulurivit on saatettu muuntaa työtilauksiksi.

Huoltoaikataulun neljä näkymää ovat hieman erilaiset sen mukaan, mitä kunnossapitoaikataulurivejä haluat nähdä.

| Valikkovaihtoehto                  | Sisällön kuvaus                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kaikki ylläpitoaikataulut       | Kaikki huoltoaikataulurivit näkyvät.     |
| Oma resurssiaikataulu        | Tässä luettelossa näkyvät kaikki huoltoaikataulurivit, jotka sisältävät käyttökohteita, jotka on asennettu toiminnallisiin siajinteihin, joihin olet yhteydessä työntekijänä ([Kunnossapitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md)). |
| Avaa ylläpitoaikataulun rivit | Tässä luettelossa näkyvät ylläpitoaikataulurivit, joiden tila on Luotu, eli niitä ei ole vielä muunnettu työtilaukseksi tai hylätty.                                            |
| Avaa ylläpitoaikataulun poolit | Tässä luettelossa näkyvät työtilauspooliin liittyvät huollonajoitusrivit.                                                                                                                  |

>[!NOTE]
>Jos huoltoaikataulurivi sisältyy useisiin työtilauspooleihin (lisätietoja on kohdassa [Työtilauspoolit](../work-orders/work-order-pools.md)), kullekin poolille näytetään yksi tietue kohdassa **Avoimet ylläpitoaikataulupoolit**. Tämä tehdään työtilauspoolien suodatusasetusten optimoimiseksi.

Ylläpitoaikataulun avaaminen:

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit**.

2. Päivitä ylläpitoaikataulu valitsemalla **Ylläpitosuunnitelma** tai **Ylläpitokierrokset.** 

3. Voit muokata huoltoaikataulun riviä valitsemalla sen ja valitsemalla sitten **Muokkaa**. Voit esimerkiksi päivittää helposti palvelutason tai työntekijän, joka vastaa työstä. Voit muokata vain sellaisia ylläpitoaikataulurivejä, joita ei ole vielä liitetty työtilaukseen.

4. Voit poistaa huoltoaikataulurivin valitsemalla sen luettelosivulta ja valitsemalla sitten **Poista**.

5. Voit hylätä huoltoaikataulurivin valitsemalla sen luettelosivulta ja valitsemalla sitten **Hylkää**. Tämä toiminto on hyödyllinen esimerkiksi silloin, kun käyttöomaisuuserään liittyy 2 000 km huoltosuunnitelma ja 10 000 km huoltosuunnitelma. Tämän jälkeen voit hylätä 2 000 km huoltosuunnitelmasta luodun rivin, kun se on sama kuin 10 000 km, 20 000 km, 30 000 km huollossa ja niin edelleen. Jos hylkäät huoltosuunnitelmaan liittyvän huoltoaikataulurivin, kyseinen rivi ei enää tule näkyviin, kun huoltosuunnitelma ajoitetaan.

6. Voit valita huoltoaikataulurivien määrän kaikissa valitsemalla **Kaikki ylläpitoaikataulut** -kohdassa **Työtilauspooli**, jos haluat, että kaikki valitut rivit sisällytetään samaan työtilauspooliin.

7. Voit valita huoltoaikataulu rivien määrän kohdassa **Kaikki ylläpitoaikataulut**, **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit** ja napsauttamalla **Säädä aikataulua**, jos haluat tehdä samat muutokset useille riveille. Voit muuttaa valittuihin huoltoaikataulu riveihin liittyviä alkamis- ja päättymispäiviä, palvelutasoa ja vastuullista ylläpitotyöntekijäryhmää tai vastuullista kunnossapitotyöntekijää.

- Kun kunnossapitoaikataulun rivi on liitetty työtilaukseen, työtilauksen tunnus näkyy **Työtilaus-** kentässä.  
- **Kaikki resurssit** -tietonäkymän **Resurssin ylläpitosuunnitelmat** -pikavälilehdessä voit valita omaisuuserän ylläpitosuunnitelmat. Jos myöhemmin poistat resurssiiin liittyvän ylläpitosuunnitelman rivin **Kaikki resurssit** -kohdassa, poistat myös automaattisesti kaikki kunnossapitoaikataulurivit, joiden tila on Luotu ja jotka on luotu kyseisen ylläpitosuunnitelman perusteella. Katso myös [Luo resurssi](../objects/create-an-object.md).

Alla olevassa kuvassa näkyy **Kaikki ylläpitoaikataulut** -luettelosivu.

![Kuva 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]