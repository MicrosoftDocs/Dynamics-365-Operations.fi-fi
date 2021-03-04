---
title: Vian lisääminen työtilaukseen
description: Tässä aiheessa kuvataan, miten vikamerkinnät lisätään työtilauksiin käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427102"
---
# <a name="add-fault-to-work-order"></a>Vian lisääminen työtilaukseen

[!include [banner](../../includes/banner.md)]



Voit lisätä vikasuunnittelijassa määritettyjä vikamäärityksiä työtilaukseen. Vähintään yhden vikatietueen on liityttävä työtilauksessa valitussa resurssissa käytettyihin resurssityyppeihin. Lisätietoja määrityksestä esitetään kohdassa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, jolle vikarekisteröinti tehdään ja valitse sitten **Resurssin vika** **Resurssi**-ryhmän **Työtilaus**-välilehden toimintoruudussa.

3. Valitse **Oireet**-pikavälilehdessä **Lisää rivi**. **Vika**-kenttään syötetään automaattisesti vian järjestysnumero.

4. Valitse asiaankuuluva oire **Vian oire** -kentässä.

5. Valitse asianmukaiset arvot kentissä **Vika-alue** ja **Vikatyyppi**.

6. **Vian päivämäärä** -kenttään valitaan automaattisesti nykyinen päivämäärä. Voit valita tarpeen mukaan eri päivämäärän.

7. Lisää **Valitun oireen syyt** -pikavälilehdessä rivi kuvaamaan ongelman syytä.

8. Lisää **Valitun oireen korjaukset** -pikavälilehdessä rivi kuvaamaan mahdollista ratkaisua ongelmaan.

9. Valitse **Tallenna**.

Alla olevassa kuvassa näkyy esimerkki vikarekisteröinnistä.

![Kuva 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Näytä resurssin viat

**Resurssin viat** -luettelossa voit saada yleiskuvan kaikista omaisuuteen rekisteröidyistä virheistä.

**Resurssin viat** -luettelosivulla voit saada yleiskuvan kaikista resursseihin rekisteröidyistä virheistä. Avaa sivu valitsemalla **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssin viat**.


## <a name="print-asset-fault-report"></a>Tulosta resurssin vikaraportti

**Kaikki resurssit** luettelosivulla voit tulostaa omaisuusvikaraportin, jossa näkyvät kaikki vikarekisteröinnit sekä graafisen yhteenveto vikatilastoista.

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit**.

2. Valitse resurssi, jolle tulostetaan vikaraportti.

3. Valitse toimintoruudun **Yleinen**-välilehden **Raportit**-ryhmässä **Resurssin vika**.

4. Syötä tietty kausi tai valitse vikatyyppi.

5. Tulosta raportti valitsemalla **OK**.

>[!NOTE]
>Voit tulostaa useiden resurssien tai resurssityyppien vikaraportin valitsemalla **Resurssien hallinta** > **Raportit** > **Resurssit** > **Resurssin vika**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]