---
title: Resurssivikojen kustannusten hallinta
description: Tässä ohjeaiheessa kerrotaan resurssivikojen kustannushallinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918300"
---
# <a name="asset-fault-cost-control"></a>Resurssivikojen kustannusten hallinta

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Käyttöomaisuuden hallinnassa voit laskea käyttöomaisuuden vikamerkintöjen kustannukset, jolloin saat yleiskuvan todellisista kustannuksista verrattuna budjetin kustannuksiin vikojen osalta. Todelliset kustannukset perustuvat kirjattuihin tapahtumiin. Päivämäärä on vikapäivämäärä, jolloin oire tallennettiin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen kustannusten hallinta**.

2. Valitse **Resurssivikojen kustannusten hallinta** -valintaikkunassa laskennassa käytettävä taloushallinnon dimensioyhdistelmä, jos se on tarpeen.

4. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin vikakustannusten valvontarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikojen kustannushallintarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät ja virheiden syyt **Sisällytettävät tietueet** -pikavälilehdessä.

7. Aloita laskenta valitsemalla **OK**.

8. Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut toimintoruudun painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

Alla olevassa kuvassa on esimerkki käyttöomaisuusvirheiden kustannustenhallinnan laskennasta.

![Kuva 1](media/05-controlling-and-reporting.png)

Lisätietoja vikojen määrittämisestä on [Vikojen hallinta](../setup-for-work-orders/fault-management.md) -osassa.

>[!NOTE]
>**Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset. **Todelliset kustannukset** -kentässä näkyvät työtilausten kirjatut kustannukset. **Sidottu kustannus** -kentässä näkyvät kokonaiskustannukset, joihin yritys on sitoutunut suhteessa työtilauksiin.

