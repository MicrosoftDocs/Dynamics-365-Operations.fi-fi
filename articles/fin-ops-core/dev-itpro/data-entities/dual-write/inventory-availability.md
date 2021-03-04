---
title: Varaston käytettävyys kaksoiskirjoituksessa
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4452191"
---
# <a name="inventory-availability-in-dual-write"></a>Varaston käytettävyys kaksoiskirjoituksessa

[!include [banner](../../includes/banner.md)]

Varaston käytettävyyttä käyttämällä voi tarkistaa varaston, ennen kuin tuote lisätään Microsoft Dynamics 365 Salesin **Tarjoukset**-, **Tilaukset**- tai **Laskut**-sivulla. Esimerkiksi varaston tarkistaminen ja täyttämispäivän määrittäminen ovat yksi [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtävistä.

Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella. Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.

## <a name="on-hand-inventory"></a>Käytettävissä oleva varasto

Dynamics 365 Salesin **Tarjous**-, **Tilaus**- ja **Lasku** -sivujen otsikkoon on lisätty uusi **Käytettävissä oleva varasto** -painike. Kun valitset tämän painikkeen, näyttöön avautuu valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jonka käytettävissä olevan varaston haluat tarkistaa. Tässä valintaikkunassa on samat tiedot kuin [käytettävissä olevassa varastossa](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Valintaikkuna palauttaa varastotiedot Dynamics 365 Supply Chain Managementista. Nämä tiedot sisältävät seuraavat määrät:

- Varastosaldo
- Varattu varastosaldo
- Käytettävissä oleva varastosaldo
- Tilattu määrä
- Tilauksessa oleva määrä
- Varattu tilattu määrä
- Käytettävissä oleva kokonaismäärä

## <a name="atp-information"></a>ATP-tiedot

Salesissa on lisätty uusi **ATP-tiedot**-painike **Tarjoukset**-, **Tilaukset**- ja **Laskut**-sivujen rivinimikkeisiin. Kun tämä painike valitaan, avautuvassa valintaikkunassa voi määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän. Tässä valintaikkunassa on samat asetukset, jotka kuvattiin kohdassa [Luvatut tilaukset](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Valintaikkuna palauttaa ATP-tiedot Supply Chain Managementissa. Nämä tiedot sisältävät seuraavat määrät:

- ATP-määrä
- Vastaanoton määrä
- Varasto-oton määrä
- Varastosaldo


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]