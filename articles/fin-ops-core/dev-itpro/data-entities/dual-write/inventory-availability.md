---
title: Varaston käytettävyys kaksoiskirjoitusalueella
description: Tässä ohjeaiheessa on tietoja varaston käytettävyyden tarkistamisesta kaksoiskirjoituksella.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426979"
---
# <a name="inventory-availability"></a>Varaston käytettävyys

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varaston käytettävyyttä käyttämällä voit tarkistaa varastosi, ennen kuin lisäät tuotteen mallisovellusten **tarjouksiin**, **tilauksiin** tai **laskuihin** Dynamics 365 -järjestelmässä. Esimerkiksi varaston tarkistaminen ja toteutuksen päättymispäivän määrittäminen ovat [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtäviä. Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella. Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.

## <a name="on-hand-inventory"></a>Käytettävissä oleva varasto 

Dynamics 365 Salesin **Tarjous**-, **Tilaus**- tai **Lasku** -lomakkeiden otsikossa on lisätty uusi **Käytettävissä oleva varasto** -painike. Kun napsautat painiketta, näyttöön tulee valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jolle haluat tarkistaa käytettävissä olevan varaston. Se palauttaa varastotiedot Dynamics 365 Supply Chain Management -lomakkeesta ja näyttää samat tiedot kuin kohteessa [käytettävissä oleva varasto](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Tiedot sisältävät seuraavat määrät:

- **Varastosaldo**
- **Varattu varastosaldo**
- **Saatavilla oleva varastosaldo**
- **Tilattu määrä**
- **Tilauksessa oleva määrä**
- **Varattu tilattu määrä**
- **Käytettävissä oleva kokonaismäärä**

## <a name="atp-information"></a>ATP-tiedot

Dynamics 365 Salesin **Tarjous**-, **Tilaus**- tai **Lasku** -lomakkeiden rivinimikkeisiin on lisätty uusi **ATP-tiedot**-painike. Kun napsautat painiketta, näyttöön tulee valintaikkuna, jossa voit määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän. Se palauttaa **ATP-tiedot** Supply Chain Managementista ja näyttää asetukset [toimituksen lupaamisen](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) osalta. Tietoihin sisältyvät **ATP-määrä**, **Vastaanottomäärä**, **Varasto-ottomäärä** ja **Käytettävissä oleva määrä**.
