---
title: Työtilaukset ja käyttöomaisuuserät
description: Tässä ohjeaiheessa selitetään, miten työtilaukset ja käyttöomaisuuserät ajoitetaan käyttöomaisuuden hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816721"
---
# <a name="work-orders-and-fixed-assets"></a>Työtilaukset ja käyttöomaisuuserät

[!include [banner](../../includes/banner.md)]


Resurssien hallinnassa resurssit voivat liittyä käyttöomaisuuseriin, ja voit luoda työtilauksia kyseisille resursseille. Jos käytät tätä toimintoa, voit saada kattavan yleiskuvan käyttöomaisuudesta, siihen liittyvistä investointiprojekteista sekä investointiprojekteihin rekisteröidyistä kustannuksista moduuleissa **Projektinhallinta ja kirjanpito** ja **Käyttöomaisuuserät** Microsoft Dynamics 365 for Finance and Operationsissa.

>[!NOTE]
>**Käyttöomaisuuden numero** -kenttä määritetään työtilauksen työprojektissa vain, jos työtilauksen työprojektin projektityypiksi on valittu **Investointi**.

Alla olevassa kuvassa näkyy **Projektinhallinta ja kirjanpito** -moduulissa olevan investointiprojektin ja työtilaustehtäväprojektin välinen suhde.

![Kuva 1](media/24-work-orders.png)

Seuraavassa menettelyssä kuvataan resurssien, työtilausten, työtilausten työprojektien ja käyttöomaisuuserien välinen suhde.

1. Luot resurssin, jonka liität käyttöomaisuuteen.

![Kuva 2](media/25-work-orders.png)

2. Kun määrität työtilaustyypit **Työtilaustyypit**-sivulla (**Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Työtilaustyypit**), luot työtilaustyypin, jolla käsitellään investointeja. Katso myös [Työtilaustyypit ](../setup-for-work-orders/work-order-types.md).

![Kuva 3](media/26-work-orders.png)

3. Kun määrität työtilausten projektiryhmiä **Työtilauksen projektiasetukset**-sivun **Projektiryhmä**-välilehdessä (**Resurssienhallinta** > **Asetukset** > **Työtilaukset** > **Projektimääritykset**), luot suhteen investointeihin käytettävän työtilaustyypin ja investoinneille **Projektinhallinta ja kirjanpito** -moduulin **Projektiryhmät**-sivulla (**Projektinhallinta ja kirjanpito** > **Asetukset** > **Kirjaus** > **Projektiryhmät**) luodun projektiryhmän välillä.

![Kuva 4](media/27-work-orders.png)

4. Kun luot käyttöomaisuuteen liittyvän työtilauksen, valitset investointien käsittelyyn käytettävän työtilaustyypin (kuten **Investointi**).

5. Kun työtilaus luodaan, siihen liittyvä työtilaustyyppi näkyy sivulla **Kaikki työtilaukset**.

![Kuva 5](media/28-work-orders.png)

6. Kun työtilaus luodaan, työtilaukseen liittyvä projekti luodaan **Kaikki projektit** -sivulla **Projektinhallinta ja kirjanpito** -moduulissa (**Projektinhallinta ja kirjanpito** > **Projektit** > **Kaikki projektit**). Jos haluat tarkastella projektiin liittyviä tietoja, valitse linkki **Projektitunnus**-kentässä **Yleistä**-välilehdessä **Rivitiedot**-pikavälilehdessä **Kaikki työtilaukset** -sivun tietonäkymässä **Resurssienhallinta** -moduulissa (**Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset**).

![Kuva 6](media/29-work-orders.png)

7. Jos haluat nähdä yhteenvedon käyttöomaisuuteen liittyvistä projekteista, valitse **Käyttöomaisuuserät** > **Käyttöomaisuuserät** > **Käyttöomaisuuserät** ja sitten **Käyttöomaisuuserän numero** -kentässä linkki käyttöomaisuudelle, joka avataan tietonäkymässä. Laajenna **Aiheeseen liittyviä tietoja** -ruutu sivun oikeassa reunassa ja valitse **Liittyvät projektit** -pikavälilehti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]