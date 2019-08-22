---
title: Saapuvat ja lähtevät resurssit
description: Tässä ohjeaiheessa kerrotaan, miten saapuvat ja lähtevät resurssit rekisteröidään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847548"
---
# <a name="inbound-and-outbound-assets"></a>Saapuvat ja lähtevät resurssit

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Jos yrityksesi tekee korjauksia tai kunnossapitotyötä muista sijainneista tai asiakkaista saatuihin resursseihin, resurssien hallinta voi seurata sekä saapuvia resursseja, jotka ovat matkalla yritykseen, että lähteviä resursseja, jotka palautetaan.

> [!NOTE]
> Jos haluat käyttää saapuvia ja lähteviä elinkaaritiloja hallitsemaan resursseja, jotka tulevat sisään ja palautetaan, sinun täytyy määrittää huoltopyynnön elinkaaritilat ja elinkaariallit tukemaan näitä toimintoja. Lisätietoja: [Ylläpitopyyntöjen määritys](../setup-for-maintenance-requests/requests.md).

Resurssien hallinnan asetukset määrittävät, voiko saapuvia ja lähteviä resursseja käsitellä.

## <a name="register-assets-as-inbound"></a>Rekisteröi resurssit saapuviksi

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.
2. Valitse ylläpitopyyntö.
3. Valitse **Päivitä ylläpitopyynnön tila**.
4. Valitse **Saapuva** (tai muu elinkaaren tila, jonka olet luonut saapuville resursseille) ja valitse sitten **OK**.

![Kuva 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Rekisteröi saapuvat resurssit vastaanotetuiksi

1. Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Saapuvat resurssit**.
2. Valitse resurssi tai ylläpitopyyntö.
3. Valitse **Vastaanota resurssit**.
4. Määritä päivämäärä ja kellonaika **Vastaanotettu**-kentässä. Valitse sitten **OK**. Tietue poistetaan **Saapuvat resurssit** -luettelosivulta.

![Kuva 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Rekisteröi resurssit lähteviksi

Kun huolto- tai korjaustyö on suoritettu, voit rekisteröidä resurssin palautetuksi.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.
2. Valitse ylläpitopyyntö.
3. Valitse **Päivitä ylläpitopyynnön tila**.
4. Valitse **Lähtevä** (tai muu elinkaaren tila, jonka olet luonut lähteville resursseille) ja valitse sitten **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Rekisteröi lähtevät resurssit toimitetuiksi

1. Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Lähtevät resurssit**.
2. Valitse resurssi tai ylläpitopyyntö.
3. Valitse **Toimita resurssit**.
4. Määritä päivämäärä ja kellonaika **Toimitettu**-kentässä. Valitse sitten **OK**. Tietue poistetaan **Lähtevät resurssit** -luettelosivulta.
