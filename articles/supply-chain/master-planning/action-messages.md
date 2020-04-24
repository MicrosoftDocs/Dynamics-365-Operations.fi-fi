---
title: Toimenpidesanomat
description: Toimintosanoma on järjestelmän luoma ehdotus olemassa olevan suunnitellun tai vahvistetun tilauksen muuttamisesta.
author: ChristianRytt
manager: tfehr
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6eb65f0cf97490177d38001e5ac793aa584f33bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203960"
---
# <a name="action-messages"></a>Toimenpidesanomat

[!include [banner](../includes/banner.md)]

Toimintosanoma on järjestelmän luoma ehdotus olemassa olevan suunnitellun tai vahvistetun tilauksen muuttamisesta.

## <a name="introduction"></a>Johdanto

Pääsuunnittelulaskenta luo toimintosanomat vaatimusten muuttuessa. Esimerkiksi lähetyspäivä tai määrä on voinut muuttua myyntitilauksessa, jolle olet jo luonut ostotilauksen kysynnän täyttämistä varten. Siinä tapauksessa pääsuunnittelun laskenta voi vähintään yhden toimintosanoman päivittämään ostotilauksen. Voit päättää, tehdäänkö ehdotetut muutokset.

Voit määrittää, millä tavalla toimintosanomat lasketaan nimikkeeseen liitettävälle kattavuusryhmälle.

## <a name="select-action-messages"></a>Toimintosanomien valitseminen

Voit valita **Kattavuusryhmät**-sivulla toimintosanomat, jotka haluat järjestelmän muodostavan sekä kattavuusryhmät tai nimikkeet, joita sanomat koskevat. Valittavana on seuraavat toimintosanomat.

| Sanoma             | Kuvaus                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aikaista**         | Jos valitset tämän sanoman, järjestelmä luo tarvittaessa toimintosanomat, joilla tilaukset siirretään aikaisemmaksi. Voit määrittää **Aikaistamisen aikaraja** -kentässä myös kuinka monta päivää vastaanoton ja varasto-oton välillä voi enintään olla ilman aikaistamistoimintoa. |
| **Lykkää**        | Jos valitset tämän sanoman, järjestelmä luo tarvittaessa toimintosanomat, joilla tilaukset siirretään myöhemmäksi. Voit määrittää **Lykkäyksen aikaraja** -kentässä kuinka monta päivää vastaanoton ja varasto-oton välillä voi enintään olla ilman lykkäystoimintoa.       |
| **Vähennä määrää**        | Jos valitset tämän sanoman, tuotantotilausten, ostotilausten ja muiden vastaanottotilausten määrän pitäisi pienentyä, jotta varastotasot eivät ylittyisi.                                                                                                   |
| **Lisää määrää**        | Jos valitset tämän sanoman, tuotantotilausten, ostotilausten ja muiden vastaanottotilausten määrän pitäisi kasvaa, jotta varastovajetta ei syntyisi.                                                                                                    |
| **Johdetut toimenpiteet** | Jos valitset tämän sanoman, johdetuille vaatimuksille luodaan toimintosanomat, kuten toiminnot tuotantoa täyttäville komponenttitilauksille.                                                                                                   |





