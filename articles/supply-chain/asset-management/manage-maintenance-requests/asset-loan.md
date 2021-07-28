---
title: Lainatut resurssit
description: Tässä ohjeaiheessa kerrotaan, miten lainatut resurssit rekisteröidään resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9be41f459b8ec8ca8ccad2360218b32299cb319e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354926"
---
# <a name="asset-loans"></a>Lainatut resurssit

[!include [banner](../../includes/banner.md)]

 

Jos yrityksesi saa resursseja korjaus-tai huoltotöihin joko sisäisistä sijainneista tai asiakkailta ja jos olet tilapäisesti lainannut resursseja kyseisille sijainteille tai asiakkaille, resurssien hallinta voi seurata resurssilainoja.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Rekisteröi kunnossapitopyynnön resurssilainat

1. Valitse **Resurssien hallinta** \> **yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt** ta **Aktiiviset ylläpitopyynnöt**.
2. Valitse ylläpitopyyntö, johon resurssilaina rekisteröidään, ja valitse sitten **Muokkaa**.
3. Valitse **Pyyntö**-sivulla **Lähetä lainaresurssi**.
4. Valitse resurssi ja syötä odotettu palautuspäivämäärä.
5. Valitse **OK**.

> [!NOTE]
> - Voit lähettää lainaresurssin vain, jos saman resurssityypin resurssi on käytettävissä.
> - Lainatulla resurssilla on oltava resurssien elinkaaritila, jonka avulla sitä voidaan käyttää lainaresurssina, kuten **InStorage**. Kun resurssilaina on rekisteröity, resurssin elinkaaren tila päivitetään automaattisesti esimerkiksi tilaan **onLoan**.

Voit tarkastella luettelosa kaikista resursseista, jotka olet lainannut muihin siajinetihin tai asiakkaille valitsemalla **Resurssien hallinta** \> **Yhteiset** \> **Resurssin laina** \> **Kaikki resurssilainat**. Jos **Päättynyt** -valintaruutu on valittuna resurssille, resurssi on rekisteröity palautetuksi yritykseesi.

![Ylläpitopyyntöjen hallinta.](media/06-manage-maintenance-requests.png)

**Aktiiviset resurssilainat** -sivulla voit tarkastella luetteloa kaikista lainavaroista, joita ei ole vielä palautettu yrityksellesi.

## <a name="register-loan-assets-as-returned"></a>Rekisteröi lainaresurssit palautetuksi

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssin laina** \> **Aktiiviset resurssilainat**.
2. Valitse resurssilaina, jonka haluat rekisteröidä palautetuksi, ja valitse sitten **Palauta resurssilaina**.
3. Määritä päivämäärä ja kellonaika **Palautettu**-kentässä.
4. Valitse **OK**.
5. Päivitä **Aktiiviset resurssilainat** -luetteloivu ja huomaa, että resurssilaina ei enää näy luettelossa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]