---
title: Resurssit ja työtilaukset
description: Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2872dc84ec11ae7fad9fd5b225b9207f13280db334cc0d010a3d6749a591ee2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718104"
---
# <a name="assets-and-work-orders"></a>Resurssit ja työtilaukset

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan resursseista ja työtilauksista resurssien hallinnassa. Resurssit ja työtilaukset ovat resurssien hallinnan keskeisiä osia. *Resurssi* on kone tai koneen osa, joka vaatii jatkuvaa ylläpitoa ja huoltoa. Resursseja voidaan luoda hierarkkisessa rakenteessa, ja ne voivat liittyä toiminnallisiin sijainteihin. Ylläpitotöitä voidaan suunnitella kaikilla resurssirakenteen tasoilla.

Eri tiedot, kuten tuotetiedot ja resurssien määritykset sekä vaaditut huoltosuunnitelmat määritetään kullekin resurssille. Seuraavassa kuvassa on yhteenveto resurssin tiedoista ja resurssien liitoksista työtyyppeihin. Punaista tekstiä käytetään esimerkeissä, jotka näyttävät periytymisen ja riippuvuudet.

![Kaavio, jossa resurssitiedot näkyvät suhteessa työtyyppeihin.](media/05-overview-image.png)

Jokaisella työtilauksella on työtilaustyyppi, kuten ennakoiva kunnossapito, korjaava kunnossapito tai tarkastus. Työtilaus sisältää vähintään yhden työtilaustyön. Jokainen työtilauksen työ määrittää työn, joka on suoritettava resurssille ja siihen liittyvälle työtyypille. Esimerkkejä liittyvistä työtyypeistä ovat 10 000 km, 50 000 km ja 1 vuoden huolto sekä turvallisuustarkastus. Yksi työtilaus voi liittyä useisiin resursseihin.

Seuraavassa kuvassa on yhteenveto työtilauksen tärkeimmistä tiedoista.

![Kaavio, jossa näkyvät työtilauksen olennaisimmat tiedot.](media/06-overview-image.png)

Työtilaus voi liittyä toiseen työtilaukseen, ja työtyypit voivat sisältää työtilauksen muodostavat seuraavat työt. Työtilausten välillä ei yleensä ole riippuvuuksia. Tämän vuoksi ne voivat muuttaa työtilauksen elinkaaren tilaa ja ne voidaan ajoittaa toisistaan riippumatta.

Työtilauksia voidaan luoda eri tavoilla, jotka liittyvät korjaaviin, ennaltaehkäiseviin tai reaktiivisiin ylläpitotöihin. Voit luoda työtilauksia myös manuaalisesti. Seuraavassa kuvassa on yleiskuvaus työtilausten automaattista tai manuaalista luomista koskevasta prosessista.

![Kaavio, jossa näkyy työtilausten automaattinen tai manuaalinen luonti.](media/07-overview-image.png)

Useita vaiheita on suoritettava, kun haluat ajoittaa ja suorittaa ylläpitotyön työtilaukselle. Seuraavassa kuvassa on yhteenveto työtilauksen käsittelystä.

![Kaavio, jossa näkyy yleiskatsaus työtilauksen prosessointiin.](media/08-overview-image.png)

> [!NOTE]
> Yleensä kun työskentelet Dynamics 365 Supply Chain Managementissa ja **Resurssien hallinta** -moduulissa, valitset **Uusi** luodaksesi uuden tietueen, valitset **Muokkaa** päivittääksesi aiemmin luodun tietueen ja valitset **Tallenna** tallentaaksesi uusia tai muokattuja tietoja.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]