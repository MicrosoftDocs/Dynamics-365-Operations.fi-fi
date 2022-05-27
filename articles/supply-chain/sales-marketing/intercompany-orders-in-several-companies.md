---
title: Konsernin sisäisten osto ja myyntitilausten luominen useissa yrityksissä
description: Tässä aiheessa käsitellään konsernin sisäisten osto- tai myyntitilausten luontia useissa yrityksissä
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8458a08c1a2e5e656c496eb74188d0e2e7257020
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673715"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Konsernin sisäisten osto ja myyntitilausten luominen useissa yrityksissä

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementissa käsittely ei rajoitu vain yhden tuotantoyrityksen ja useiden myyntiyritysten käsittelyyn. Kaikki yritykset, joka on määritetty konsernin sisäisiksi, voivat toimia sekä ostoyrityksinä että myyntiyrityksinä.

Jos useat yritykset voivat toimittamaan samaa nimikettä, voit valita vapaasti yrityksen, jolta nimike ostetaan. Päivitykset käsitellään, vaikka yhdestä myyntitilauksesta tulisi monta ostotilausta.

Samalla tavalla kuin luot automaattisesti konsernin sisäisenostotilauksen, voit luoda alkuperäisen myyntitilauksen omassa yrityksessä ja antaa tilauksen usean saman konsernin toimittajayrityksen toimitettavaksi luomalla useita konsernin sisäisiä ostotilauksia. Microsoft Dynamics 365 Supply Chain Management luo automaattisesti konsernin sisäiset myyntitilaukset toimittajayrityksissä.

Tätä varten kaikki yritykset on määritettävä kauppakumppanuuksina. Toimittajayritykset on määritettävä Microsoft Dynamics 365 Supply Chain Managementissa konsernin sisäisinä toimittajina, ja niiden on oltava soveltuvan nimikkeen ensisijainen toimittaja. Myyntitilauksen **otsikkonäkymässä** on valittava **Luo konsernin sisäiset tilaukset automaattisesti**- ja **Suoratoimitus**-kenttä **Konsernin sisäiset asetukset** -pikavälilehdessä: Tämä on oletusasetus.

Myyntirivit luodaan tavalliseen tapaan. Kun poistut tietueesta, näyttöön avautuu sanoma, jossa ilmoitetaan, että konsernin sisäiset osto- ja myyntitilaukset sekä linkit uusiin tilauksiin on luotu. Sanoma sisältää linkit uusiin tilauksiin. Toimittajayrityksessä luotuja konsernin sisäisiä myyntitilauksia voi tarkastella avaamalla alkuperäinen myyntitilaus ja valitsemalla **Yleiset**-välilehden **Liittyvät tiedot** -ryhmässä **Viitteet**.

Jos toimittajien konsernin sisäiset ostotilaukset avataan, havaitaan, että Microsoft Dynamics 365 Supply Chain Management täyttää alkuperäisen myyntitilausnumeron sekä konsernin sisäisen myyntitilausnumeron automaattisesti kullekin toimittajalle.

Vastaavasti jos toimittajien konsernin sisäiset myyntitilaukset avataan, havaitaan, että Microsoft Dynamics 365 Supply Chain Management täyttää alkuperäisen myyntitilausnumeron sekä konsernin sisäisen ostotilausnumeron automaattisesti kullekin toimittajalle.

> [!NOTE]
> Jos tilauksen nimikkeet ovat olemassa yhdessä konsernin sisäisessä toimittajayrityksessä mutta eivät toisessa, Microsoft Dynamics 365 Supply Chain Management luo toimittajayritykselle konsernin sisäiset tilaukset, joissa nimikkeet ovat olemassa, mutta pysäyttää tilauksen luonnin toiselle yritykselle. Ilmoitus avautuu, kun näin tapahtuu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
