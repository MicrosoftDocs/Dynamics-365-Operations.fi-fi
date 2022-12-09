---
title: Kestoltaan avoimen loman luominen
description: Tässä artikkelissa selitetään kestoltaan avoimen loman luominen Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805338"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Kestoltaan avoimen loman luominen

> [!IMPORTANT]
> Tässä artikkelissa kuvailtu toiminto tulee olemaan käytössä osana Finance-infrastruktuurin tulevaa versiota Microsoft Dynamics 365 Finance -julkaisun 10.0.31 jälkeen.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voit lähettää kestoltaan avoimia lomia koskevan pyynnön ja tarkastella lomapyyntöjen tilaa Dynamics 365 Human Resourcesissa.

## <a name="prerequisites"></a>Edellytykset

1. Varmista kohdassa **Toimintojen hallinta**, että **Kestoltaan avoin loma** -ominaisuus on käytössä.

    > [!IMPORTANT]
    > Kun toiminto on otettu käyttöön, sitä ei voi poistaa käytöstä.

2. Luo loman lomatyyppi.
3. Syötä tiedot kuten loman tyyppi, kuvaus ja työnkulun tunnus.
4. Valitse **Pyyntötyyppi**-kentässä **Virkavapaa**.
5. Kestoltaan avoimien tapauksessa määritä **Kestoltaan avoimet** -vaihtoehto arvoon **Kyllä**.
6. Määritä **Ilmoitus työhön palaamisesta** -vaihtoehto arvoon **Kyllä** tai **Ei**.
7. Ilmoitusta työhön palaamisesta voidaan tarvittaessa vaatia kestoltaan avointa lomaa pyydettäessä.

> [!NOTE]
> Kun tämä ominaisuus on otettu käyttöön, **Liite pakollinen** -ominaisuus on otettu käyttöön.

## <a name="request-an-open-ended-leave-of-absence"></a>Kestoltaan avoimen loman pyytäminen

1. Valitse **työntekijän itsepalvelu** -työtilan **Vapaasaldot** -ruudussa kohta **Lisää (...)**.
2. Jos haluat lähettää virkavapaapyynnön, valitse **Pyydä virkavapaata**.
3. Syötä tiedot kenttiin **lomatyyppi** ja **alkamispäivämäärä**. Syötä **Päättymispäivämäärä**-kenttään alustava päättymispäivämäärä.
4. Jos sinun on toimitettava tukiasiakirjoja, valitse **Liitteet**-kohdasta **Lataa**.
5. Jos olet valmis lähettämään pyyntösi, valitse **Lähetä**. Muussa tapauksessa valitse **Tallenna vedos**.
6. Jos haluat päivittää kestoltaan avoimen loman pyynnön, syötä päättymispäivämäärä **Päättymispäivämäärä**-kenttään, määritä **Vahvista päättymispäivämäärä** -vaihtoehto arvoon **Kyllä** ja lataa asiakirjat.
7. Jos **Ilmoitus työhön palaamisesta** -vaihtoehto on määritetty arvoon **Kyllä**, valitse **Lataa** ja valitse sitten valintaruutu vahvistaaksesi, että kelvollinen ilmoitus työhön palaamisesta on ladattu.
8. Kun kaikki tiedot on syötetty, valitse **Lähetä**.
