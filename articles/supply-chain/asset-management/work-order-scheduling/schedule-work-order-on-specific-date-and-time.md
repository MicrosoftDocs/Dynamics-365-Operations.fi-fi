---
title: Työtilauksen ajoittaminen tiettyyn päivämäärään ja aikaan
description: Tässä ohjeaiheessa selitetään, kuinka voit ajoittaa työtilauksen tiettyyn päivämäärään ja kellonaikaan käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28ade5bb6a22b9d15380085ea479e79ba246c1e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354057"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Työtilauksen ajoittaminen tiettyyn päivämäärään ja aikaan

[!include [banner](../../includes/banner.md)]

 

Jos työtilaus pitää ajoittaa tiettynä päivämääränä *ja* kellonaikana, voit ohittaa vakioajoitusprosessin käyttöomaisuuden hallinnassa ja luoda työtilaukselle erityisen aikataulun.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Napsauta työtilausluettelossa **Työtilaus**- sarakkeessa olevaa työtilauksen tunnusta.

3. Valitse **Muokkaa**.

4. Lisää **Työtilauksen otsikko** -pikavälilehdellä alkamis- ja päättymispäivämäärät ja -ajat **Odotettu alkamispäivämäärä** -ja **Odotettu loppupäivämäärä** -kenttiin.

    ![Kuva 1.](media/05-work-order-scheduling.png)

5. Valitse **Yleiset**-välilehdessä **Ajoitus**, jos haluat käyttää vakioajoitusprosessia, tai valitse **Resursoi**, jos aiot kohdentaa työtilauksen tietylle työntekijälle.

6. Jos haluat ohittaa kaikki olemassa olevat kapasiteettivaraukset ja varmistaa, että työtilaus ajoitetaan odotettuun ajanjaksoon, tee valinnat alla olevan kuvan mukaan **Ajoita työtilaus** -valintaikkunan **Rajallinen kapasiteetti** -osassa. Tämä tarkoittaa, että ajoittaminen ohittaa olemassa olevat kapasiteettivaraukset, koska työtilauksen täytyy alkaa odotetusta alkamisajasta.

    ![Kuva 2.](media/06-work-order-scheduling.png)

7. Aloita ajoitus valitsemalla **OK**.

8. Jos ajoittaminen aiheuttaa kaksinkertaisia varauksia, näytössä näkyy sanoma ja siihen liittyviä työtilauksia voi muuttaa.

>[!NOTE]
>Jotta huoltotyöntekijä voidaan ajoittaa työtilauksen, kyseisen huoltotyöntekijän on oltava käytettävissä odotettuna alkamispäivänä ja aikana. Työntekijän käytettävyys määritetään [Työntekijän kalenterissa](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]