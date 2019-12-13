---
title: Pääsuunnittelun aloitussivu
description: Pääsuunnittelun avulla yritykset voivat määrittää tulevan raaka-aineiden ja kapasiteetin tarpeen ja tasapainottaa ne yrityksen tavoitteita vastaaviksi.
author: ShylaThompson
manager: AnnBe
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0588ad24cb28a32557361e1a2e5391502a8b46d7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814258"
---
# <a name="master-planning-home-page"></a>Pääsuunnittelun aloitussivu

[!include [banner](../includes/banner.md)]

Pääsuunnittelun avulla yritykset voivat määrittää tulevan raaka-aineiden ja kapasiteetin tarpeen ja tasapainottaa ne yrityksen tavoitteita vastaaviksi. Pääsuunnittelussa arvioidaan seuraavat seikat: 

-  Mitkä raaka-aineet ja kapasiteetit ovat tällä hetkellä käytettävissä? 
-  Mitkä ovat tuotannon valmistumisessa tarvittavat raaka-aineet ja kapasiteetit? Esimerkiksi mitä on valmistettava, ostettava, siirrettävä tai asetettava varmuusvarastoon, ennen kuin tuotanto saadaan valmiiksi.

Pääsuunnittelu laskee tarpeet ja luo suunnitellut tilaukset näiden tietojen avulla.

Kolme pääsuunnitteluprosessia ovat seuraavat:

-  **Pääsuunnittelu** - pääsuunnitelma laskee nettotarpeet. Se perustuu toteutuneet tämän hetkisiin tilauksiin. Tämän avulla yritykset voivat ohjata varaston täydennystä lyhyellä aikavälillä päivittäin. Pääsuunnittelua kutsutaan myös *nettotarvesuunnitelmaksi*. Lisätietoja on kohdassa [Pääsuunnitelmien yleiskatsaus](master-plans.md). 

-  **Ennusteen suunnittelu** - ennusteajoitus laskee bruttotarpeet. Se perustuu tuleviin arvioihin (tai ennusteisiin). Yritykset voivat käyttää tätä materiaalien ja kapasiteetin pitkäaikaissuunnittelussa. Lisätietoja on kohdassa [Kysynnän ennusteen yleiskatsaus](introduction-demand-forecasting.md). 

-  **Konsernin sisäinen pääsuunnittelu** - Konsernin sisäinen pääsuunnitelma laskee yritysten nettotarpeet. Se yhdistää kysynnän ja tarjonnan yritysten välillä niin lyhytaikaisen, kiinteän kysynnän ja tarjonnan kuin myös pitkäaikaisen ja suunnitellun (mutta ei vielä kiinteän) kysynnän ja tarjonnan osalta. Lisätietoja on kohdassa [Konsernin sisäinen pääsuunnittelu](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (eLearning) (vaatii CustomerSource-tilin). 

Yritykset voivat muuttaa suunnitelman tulosta. Yritykset voivat suorittaa uudelleensuunnittelun, nettomuutoksen tai molemmat. Uudelleensuunnittelut päivittävät kaikki vaatimukset, kun taas nettomuutossuunnitelmat päivittävät vain suunnitelman, jonka nimikkeille on määritetty uusia tarpeita edellisen ajoituksen jälkeen.

Pääajoituksen suunnitelmat ovat yleensä lyhytaikaisia. Tämä voi tarkoittaa mitä tahansa aikaa viikosta kuuteen kuukauteen. Pääsuunnittelumoduuli määrittää tarjonnan (materiaalit) ja kapasiteetin (resurssit) tarpeen, joka vastaa nykyistä kysyntää (nettovaatimukset). Useimmissa yrityksissä tämä on laajennettu käsittämään pisin kumulatiivinen läpimenoaika, jonka aikana tuotteet vastaanotetaan.

## <a name="learning-map"></a>Oppimiskartta

Seuraavassa oppimiskartassa on esillä tärkeitä käsitteitä ja tehtäviä, joista pääsuunnittelumoduulin kehys koostuu. Opi käyttämään moduulia [Pikalinkit](#quick-links)-osion linkeistä.

[![Pääsuunnittelun oppimiskartta](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Pikalinkit

- [Pääsuunnitelmien yleiskatsaus](master-plans.md)  
- [Rajoitetun suunnitelman luominen](./tasks/constrained-plan.md)
- [Rinnakkaistuotteiden materiaalisuunnitelman luominen](./tasks/create-material-plan-co-products.md)
- [Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)
- [Konserniyritysten välisen suunnitelman luominen](./tasks/create-intercompany-plan.md)
- [Kysynnän ennustepalveluiden yleiskatsaus](introduction-demand-forecasting.md)
- [Ennusteen vähennysavaimet](reduction-keys.md)
                                  
## <a name="additional-resources"></a>Lisäresurssit

### <a name="roadmaps"></a>Tiekartat
[Microsoft Dynamics 365 Tiekartta](https://roadmap.dynamics.com/) -sivustolla on lisätietoja julkaistuista ja kehitteillä olevista uusista toiminnoista.

### <a name="blogs"></a>Blogit
Pääsuunnittelua sekä muita ratkaisuja koskevia mielipiteitä, uutisia ja muita tietoja on kohdissa [Dynamics AX:n valmistuksen tutkimus- ja kehitysryhmän blogi](https://blogs.msdn.microsoft.com/axmfg) ja [Dynamics AX:n toimitusketjun hallinnan tutkimus- ja kehitysryhmän blogi](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Tehtäväoppaat
Lisäohjeita on saatavilla tehtävän ohjauksina. Voit avata tehtäväoppaan napsauttamalla **Ohje**-painiketta millä tahansa sivulla.

### <a name="webinars"></a>Verkkoseminaarit
[Azuren koneoppimisen käyttäminen kysynnän ennusteessa](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Teknisen konferenssin tallenteet
-  [Kysynnän ennustetoimintojen laajentaminen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Pääsuunnittelu – vihjeitä suorituskyvyn vianmääritykseen](https://youtu.be/7v8BPmEs9Dg)
-  [Apua! Tarvesuunnittelu toimii hitaasti.](https://youtu.be/RLXybx20B5o)



