---
title: Työtilaukset ja käyttöomaisuuserät
description: Tässä ohjeaiheessa selitetään, miten työtilaukset ja käyttöomaisuuserät ajoitetaan käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875624"
---
# <a name="work-orders-and-fixed-assets"></a>Työtilaukset ja käyttöomaisuuserät


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Resurssien hallinnassa resurssit voivat liittyä käyttöomaisuuseriin, ja voit luoda työtilauksia kyseisille resursseille. Jos käytät tätä toimintoa, voit saada kattavan yleiskuvan käyttöomaisuudesta, siihen liittyvistä investointiprojekteista sekä **Projektinhallinta ja kirjanpito** -moduulin investointiprojekteihin rekisteröidyistä kustannuksista sekä **Käyttöomaisuuserät**-moduulissa Dynamics 365 for Finance and Operationsissa.

>[!NOTE]
>**Käyttöomaisuus erän numero** -kenttä täytetään työtilauksen työprojektissa vain, jos työtilauksen työprojektin projektityypiksi on valittu "investointi".

![Kuva 1](media/24-work-orders.png)

Seuraavassa menettelyssä kuvataan resurssien, työtilausten, työtilausten työprojektien ja käyttöomaisuuserien välinen suhde.

1. Luot käyttöomaisuuserään liittyvän resurssin alla olevan kuvan osoittamalla tavalla.

![Kuva 2](media/25-work-orders.png)

2. Kun määrität työtilaustyypit (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Työtilaustyypit**), luot työtilaustyypin, jolla käsitellään investointeja. Katso myös [Työtilaustyypit ](../setup-for-work-orders/work-order-types.md).

![Kuva 3](media/26-work-orders.png)

3. Kun määrität työtilausten projektiryhmät (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset** > **Projektiryhmä**-linkki), luot suhteen investointeihin käytettävän työtilaustyypin ja investoinneille **Projektinhallinta ja kirjanpito** -moduulissa (**Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Projektiryhmät**) luodun projektiryhmän välillä.

![Kuva 4](media/27-work-orders.png)

4. Kun luot käyttöomaisuusobjektiin liittyvän työtilauksen, valitset sijoitusten käsittelyyn käytettävän työtilaustyypin, esimerkiksi "investointi".

5. Kun työtilaus luodaan, siihen liittyvä työtilaustyyppi näkyy kohdassa **Kaikki työtilaukset**.

![Kuva 5](media/28-work-orders.png)

6. Kun työtilaus luodaan, työtilaukseen liittyvä projekti luodaan kohdassa **Projektinhallinta ja kirjanpito** > **Kaikki projektit**. Voit tarkastella projektiin liittyviä tietoja napsauttamalla työtilauksen **Projektitunnus**-linkkiä (**Resurssien hallinta**, avaa työtilaus Tiedot-näkymässä > **Rivin tiedot** -pikavälilehti > **Yleiset** -välilehti > **Projektitunnus**-kenttä).

![Kuva 6](media/29-work-orders.png)

7. **Käyttöomaisuuserät**-kohdassa näkyy yhteenveto käyttöomaisuuserään liittyvistä projekteista (**Käyttöomaisuuserät** > **Käyttöomaisuuserät** > **Käyttöomaisuuserät** > valitse **Käyttöomaisuuserän numero** -kentässä erä ja> tarkastele **Aiheeseen liittyvät tiedot**-ruudun sisällössä kohtaa **Liittyvät projektit**).

