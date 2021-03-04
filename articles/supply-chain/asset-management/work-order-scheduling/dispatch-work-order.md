---
title: Työtilauksen resursointi
description: Tässä ohjeaiheessa selitetään, miten työtilaus resursoidaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d46beb04923d06aa8ccec05355731aa1b3f27c5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426897"
---
# <a name="dispatch-work-order"></a>Työtilauksen resursointi

[!include [banner](../../includes/banner.md)]

 

Voit ajoittaa yhden työtilauksen tai työtilauksen työt yhdelle työntekijälle **Resursoi**-toiminnon avulla.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus luettelosta.

3. Valitse **Yleiset**-välilehdestä **Resursoi**.

4. Valitse **Ajoita työtilaus** -valintaikkunassa työntekijä **Työntekijä**-kentästä.

5. **Ajoita tunnit** -kenttään voit lisätä odotettuja työtunteja, jos odotettavissa oleva työaika poikkeaa ennustetunneista.

6. **Ajoitettu aloitus** -kenttään voit tarvittaessa muokata aloituspäivämäärää ja aikaa.

7. Jos ajoitusprosessissa on huomioitava muiden töiden jo ajoitettujen resurssien kapasiteettirajoitukset, varmista, että **Resurssi**, **Työkalu** ja **Työntekijä**-vaihtopainikkeiden arvoksi on määritetty **Kyllä.** Jos haluat nähdä yksityiskohtaisia tietoja aikataulutuksesta, valitse **Kyllä** **Yksityiskohtainen**-vaihtopainikkeessa. Tämä tarkoittaa, että työtilauksen laskettujen pisteiden tiedot näytetään infolokissa.

8. Valitse **Kyllä** **Ohita aikataulu** -vaihtopainikkeessa, jos haluat ohittaa kalenterin suljetut päivät (koskee käyttöomaisuus erää, työntekijää ja työkaluja). Valitse **Kyllä** **Ohita ajoitettu suoritus** -vaihtopainikkeessa, jos haluat ohittaa rajoitukset, jotka on mahdollisesti valittu työtilaukselle ajoituksen osalta. 

    Ajoitetun suorituksen määrityksestä on lisätietoja osassa [Ajoitettu suoritus](../setup-for-work-orders/scheduled-execution.md).

9. Valitse **OK**. Työtilauksen elinkaaren tila päivittyy automaattisesti **Ajoitettu**-elinkaaritilaan, joka on määritetty kohdassa **Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Elinkaarimallit**.

Alla olevassa kuvassa näkyy esimerkki resursointivalinnoista **Ajoita työtilaus** -valintaikkunassa.

![Kuva 1](media/04-work-order-scheduling.png)

[!NOTE]
Jos haluat poistaa aikataulun työtilauksesta, valitse työtilaus kohdassa **Kaikki työtilaukset** ja valitsemalla **Yleiset**-välilehdestä **Poista ajoitus**. Muista päivittää työtilauksen elinkaaritila manuaalisesti, jos poistat aikataulun.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]