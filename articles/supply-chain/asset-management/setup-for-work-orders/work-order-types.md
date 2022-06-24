---
title: Työtilaustyypit
description: Tässä artikkelissa selitetään työtilaustyypit käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12745960f903ebc14208f2c8a01f076ed27a38d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891173"
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

![Työtilaustyypit.](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]