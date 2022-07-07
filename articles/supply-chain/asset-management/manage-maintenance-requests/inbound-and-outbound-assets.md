---
title: Saapuvat ja lähtevät resurssit
description: Tässä artikkelissa kerrotaan, miten saapuvat ja lähtevät resurssit rekisteröidään resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016533"
---
# <a name="inbound-and-outbound-assets"></a>Saapuvat ja lähtevät resurssit

[!include [banner](../../includes/banner.md)]

 

Jos yrityksesi tekee korjauksia tai kunnossapitotyötä muista sijainneista tai asiakkaista saatuihin resursseihin, resurssien hallinta voi seurata sekä saapuvia resursseja, jotka ovat matkalla yritykseen, että lähteviä resursseja, jotka palautetaan.

> [!NOTE]
> Jos haluat käyttää saapuvia ja lähteviä elinkaaritiloja hallitsemaan resursseja, jotka tulevat sisään ja palautetaan, sinun täytyy määrittää huoltopyynnön elinkaaritilat ja elinkaariallit tukemaan näitä toimintoja. Lisätietoja on kohdassa [Ylläpitopyynnöt](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Resurssien hallinnan asetukset määrittävät, voiko saapuvia ja lähteviä resursseja käsitellä.

## <a name="register-assets-as-inbound"></a>Rekisteröi resurssit saapuviksi

1. Valitse **Resurssien hallinta** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.
2. Valitse ylläpitopyyntö.
3. Valitse **Päivitä ylläpitopyynnön tila**.
4. Valitse **Saapuva** (tai muu elinkaaren tila, jonka olet luonut saapuville resursseille) ja valitse sitten **OK**.

![Rekisteröi resurssit saapuviksi.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Rekisteröi saapuvat resurssit vastaanotetuiksi

1. Valitse **Resurssien hallinta** \> **Saapuva/lähtevä** \> **Saapuvat resurssit**.
2. Valitse resurssi tai ylläpitopyyntö.
3. Valitse **Vastaanota resurssit**.
4. Määritä päivämäärä ja kellonaika **Vastaanotettu**-kentässä. Valitse sitten **OK**. Tietue poistetaan **Saapuvat resurssit** -luettelosivulta.

![Rekisteröi saapuvat resurssit vastaanotetuiksi.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Rekisteröi resurssit lähteviksi

Kun huolto- tai korjaustyö on suoritettu, voit rekisteröidä resurssin palautetuksi.

1. Valitse **Resurssien hallinta** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.
2. Valitse ylläpitopyyntö.
3. Valitse **Päivitä ylläpitopyynnön tila**.
4. Valitse **Lähtevä** (tai muu elinkaaren tila, jonka olet luonut lähteville resursseille) ja valitse sitten **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Rekisteröi lähtevät resurssit toimitetuiksi

1. Valitse **Resurssien hallinta** \> **Saapuva/lähtevä** \> **Lähtevät resurssit**.
2. Valitse resurssi tai ylläpitopyyntö.
3. Valitse **Toimita resurssit**.
4. Määritä päivämäärä ja kellonaika **Toimitettu**-kentässä. Valitse sitten **OK**. Tietue poistetaan **Lähtevät resurssit** -luettelosivulta.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]