---
title: "Saman erän varaaminen myyntitilausta varten"
description: "Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1b63173d1efe45bf048b9c2eed4dc6250c9ee9f1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Saman erän varaaminen myyntitilausta varten

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.

Saman erän varaamisen avulla voit varata myyntitilausriville varaston yhden varastoerän mukaan. Tapettia tilaava asiakas voi esimerkiksi pyytää koko tilauksen samasta erästä saadakseen keskenään samanlaisia tapettirullia. Voit määrittää tuotteen käyttämään saman erän varausta ottamalla käyttöön seuraavat asetukset tuotteeseen liitetyssä nimikemalli-, seurantadimensio- ja varastodimensioryhmässä:

-   **Nimikemalliryhmät** – Nimikemalliryhmässä on valittava varastokäytäntöjen **Varaus**-kenttäryhmän **Saman erän valinta**- ja **Konsolidoi tarve** -kenttä.
-   **Seurantadimensioryhmät** – Seurantadimensioryhmässä on valittava eränumeron **Kattavuussuunnitelma dimension mukaan** -kenttä.
-   **Varastodimensioryhmät** – Varastodimensioryhmässä on valittava **Toimipaikka**- ja **Varasto**-kohdassa **Kattavuussuunnitelma dimension mukaan** -kenttä.

Kun varaat myyntitilausrivin tuotteelle varaston, jolla on määritetty saman erän valinta, Microsoft Dynamics 365 for Operations yrittää varata tilatun määrän yhdestä varastoerästä. Myös muut erämääritteen vaatimukset otetaan huomioon. Jos määrää ei voida täyttää yhdestä erästä, **Saman erävarauksen ristiriita** -sivu aukeaa. Sivulla kerrotaan ongelmista ja toimenpiteistä, joiden avulla varauksen tekemistä voi jatkaa. Seuraavat tilanteet saattavat estää erän varaamisen:

-   Myynnin erän käsittelykoodin **Estä varaaminen** -kohdan arvoksi on merkitty **Estetty**.
-   Erä on vanhentunut vanhentumispäivän ja mahdollisten käytettävissä olevien asiakkaan myyntipäivien perusteella. Nimikkeen varausta voidaan silti harkita, jos kyseessä on päivämäärän mukaan ohjatun FEFO-nimikkeen nimikemalliryhmä ja parasta ennen -päivä on valittu keräysehdoksi.
-   Erällä ei ole jäljellä riittävästi varastointiaikaa vanhentumispäivän ja parasta ennen -päivän sekä mahdollisten asiakkaan myyntipäivien perusteella.





