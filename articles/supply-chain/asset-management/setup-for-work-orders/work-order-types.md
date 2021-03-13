---
title: Työtilaustyypit
description: Tässä ohjeaiheessa selitetään työtilaustyypit käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9111ffa552059883696cf8248a02dfe70bc12ee7
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021526"
---
# <a name="work-order-types"></a>Työtilaustyypit

[!include [banner](../../includes/banner.md)]

 

Työtilaustyyppejä käytetään työtilausten luokituksessa. Sinulla voi esimerkiksi olla työtilauksia, jotka liittyvät ennakoivaan tai korjaavaan ylläpitoon.

Työtilaustyyppi määrittää liitoksen työtilauksen elinkaarimalliin. Työtilauksen elinkaarimalli määrittää työtilauksen elinkaaritilat, jotka voidaan määrittää työtilaukselle. (Esimerkkejä työtilausten elinkaaritiloista ovat **Luotu**, **Käynnissä** ja **Valmis**.)

Lisätietoja työtilausten elinkaaritiloista ja projektin vaiheista on kohdassa [Työtilauksen elinkaaren tilat](work-order-lifecycle-states.md).

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Työtilaustyypit**.
2. Luo uusi työtilaustyyppi valitsemalla **Uusi**.
3. Kirjoita **Työtilaustyyppi** -kenttään työtilaustyypin tunnus.
4. Anna nimi **Nimi**-kenttään.
5. Valitse elinkaarimalli **Työtilauksen elinkaarimalli** -kentässä.
5. Määritä **Yksi ylläpitotyöntekijä** -asetukseksi **Kyllä**, jos kaikki tämän tyypin työtilaukseen liittyvät työtilaustyöt ajoitetaan samalle kunnossapitotyöntekijälle.
6. Valitse **Kustannustyyppi**-kentässä tarvittaessa **korjaava**, **ennaltaehkäisevä** tai **investointi**. Kaikilla työtilauksen työtilaustöillä on oltava sama kustannustyyppi.
7. Määritä **Pakollinen**-osassa asetuksiksi **Kyllä**, jos haluat määrittää, mitkä vikaan liittyvät tai kunnossapitoon liittyvät tiedot lisätään tämäntyyppiseen työtilaukseen.

    > [!NOTE]
    > **Pakollinen**-osan vaihtoehdot liittyvät **Työtilauksen elinkaaren tilat** -sivun **Vahvista**-pikavälilehteen(**Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Elinkaaren tilat**).

8. Valitse **Tallenna**.

![Työtilaustyypit](media/16-setup-for-work-orders.png)
