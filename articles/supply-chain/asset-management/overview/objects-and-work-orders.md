---
title: Resurssit ja työtilaukset
description: Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783232"
---
# <a name="assets-and-work-orders"></a>Resurssit ja työtilaukset

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa. Resurssit ja työtilaukset ovat resurssien hallinnan keskeisiä osia. *Resurssi* on kone tai koneen osa, joka vaatii jatkuvaa ylläpitoa ja huoltoa. Resursseja voidaan luoda hierarkkisessa rakenteessa, ja ne voivat liittyä toiminnallisiin sijainteihin. Ylläpitotöitä voidaan suunnitella kaikilla resurssirakenteen tasoilla.

Eri tiedot, kuten tuotetiedot ja resurssien määritykset sekä vaaditut huoltosuunnitelmat määritetään kullekin resurssille. Seuraavassa kuvassa on yhteenveto resurssin tiedoista ja resurssien liitoksista työtyyppeihin. Punaista tekstiä käytetään esimerkeissä, jotka näyttävät periytymisen ja riippuvuudet.

![Kuva 1](media/05-overview-image.png)

Jokaisella työtilauksella on työtilaustyyppi, kuten ennakoiva kunnossapito, korjaava kunnossapito tai tarkastus. Työtilaus sisältää vähintään yhden työtilaustyön. Jokainen työtilauksen työ määrittää työn, joka on suoritettava resurssille ja siihen liittyvälle työtyypille. Esimerkkejä liittyvistä työtyypeistä ovat 10 000 km, 50 000 km ja 1 vuoden huolto sekä turvallisuustarkastus. Yksi työtilaus voi liittyä useisiin resursseihin.

Seuraavassa kuvassa on yhteenveto työtilauksen tärkeimmistä tiedoista.

![Kuva 2](media/06-overview-image.png)

Työtilaus voi liittyä toiseen työtilaukseen, ja työtyypit voivat sisältää työtilauksen muodostavat seuraavat työt. Työtilausten välillä ei yleensä ole riippuvuuksia. Tämän vuoksi ne voivat muuttaa työtilauksen elinkaaren tilaa ja ne voidaan ajoittaa toisistaan riippumatta.

Työtilauksia voidaan luoda eri tavoilla, jotka liittyvät korjaaviin, ennaltaehkäiseviin tai reaktiivisiin ylläpitotöihin. Voit luoda työtilauksia myös manuaalisesti. Seuraavassa kuvassa on yleiskuvaus työtilausten automaattista tai manuaalista luomista koskevasta prosessista.

![Kuva 3](media/07-overview-image.png)

Useita vaiheita on suoritettava, kun haluat ajoittaa ja suorittaa ylläpitotyön työtilaukselle. Seuraavassa kuvassa on yhteenveto työtilauksen käsittelystä.

![Kuva 4](media/08-overview-image.png)

> [!NOTE]
> Yleensä kun työskentelet Microsoft Dynamics 365 for Finance and Operationsissa ja **Resurssien hallinta** -moduulissa, valitset **Uusi** luodaksesi uuden tietueen, valitset **Muokkaa** päivittääksesi aiemmin luodun tietueen ja valitset **Tallenna** tallentaaksesi uusia tai muokattuja tietoja.
