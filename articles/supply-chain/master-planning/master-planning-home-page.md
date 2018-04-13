---
title: "Pääsuunnittelun aloitussivu"
description: "Pääsuunnittelun avulla yritykset voivat määrittää tulevan raaka-aineiden ja kapasiteetin tarpeen ja tasapainottaa ne yrityksen tavoitteita vastaaviksi."
author: YuyuScheller
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ed011fa1c1aa35b4a401d51bffc6af19395577
ms.openlocfilehash: 030579ac73d6333ac4ed55433b9679a58247c088
ms.contentlocale: fi-fi
ms.lasthandoff: 02/13/2018

---

# <a name="master-planning-home-page"></a>Pääsuunnittelun aloitussivu

[!INCLUDE [banner](../includes/banner.md)]

Pääsuunnittelun avulla yritykset voivat määrittää tulevan raaka-aineiden ja kapasiteetin tarpeen ja tasapainottaa ne yrityksen tavoitteita vastaaviksi. Pääsuunnittelussa arvioidaan seuraavat seikat: 

-  Mitkä raaka-aineet ja kapasiteetit ovat tällä hetkellä käytettävissä? 
-  Mitkä ovat tuotannon valmistumisessa tarvittavat raaka-aineet ja kapasiteetit? Esimerkiksi mitä on valmistettava, ostettava, siirrettävä tai asetettava varmuusvarastoon, ennen kuin tuotanto saadaan valmiiksi.

Pääsuunnittelu laskee tarpeet ja luo suunnitellut tilaukset näiden tietojen avulla.

Kolme pääsuunnitteluprosessia ovat seuraavat:

-  **Pääsuunnittelu** - pääsuunnitelma laskee nettotarpeet. Se perustuu toteutuneet tämän hetkisiin tilauksiin. Tämän avulla yritykset voivat ohjata varaston täydennystä lyhyellä aikavälillä päivittäin. Pääsuunnittelua kutsutaan myös *nettotarvesuunnitelmaksi*. Lisätietoja on kohdassa [Pääsuunnitelma](master-plans.md). 

-  **Ennusteen suunnittelu** - ennusteajoitus laskee bruttotarpeet. Se perustuu tuleviin arvioihin (tai ennusteisiin). Yritykset voivat käyttää tätä materiaalien ja kapasiteetin pitkäaikaissuunnittelussa. Lisätietoja on kohdassa [Ennusteen suunnittelu](introduction-demand-forecasting.md). 

-  **Konsernin sisäinen pääsuunnittelu** - Konsernin sisäinen pääsuunnitelma laskee yritysten nettotarpeet. Se yhdistää kysynnän ja tarjonnan yritysten välillä niin lyhytaikaisen, kiinteän kysynnän ja tarjonnan kuin myös pitkäaikaisen ja suunnitellun (mutta ei vielä kiinteän) kysynnän ja tarjonnan osalta. Lisätietoja on kohdassa [Konsernin sisäinen pääsuunnittelu](https://mbspartner.microsoft.com/AX/CourseOverview/1276)  (eLearning) (vaatii CustomerSource-tilin). 

Yritykset voivat muuttaa suunnitelman tulosta. Yritykset voivat suorittaa uudelleensuunnittelun, nettomuutoksen tai molemmat. Uudelleensuunnittelut päivittävät kaikki vaatimukset, kun taas nettomuutossuunnitelmat päivittävät vain suunnitelman, jonka nimikkeille on määritetty uusia tarpeita edellisen ajoituksen jälkeen.

Pääajoituksen suunnitelmat ovat yleensä lyhytaikaisia. Tämä voi tarkoittaa mitä tahansa aikaa viikosta kuuteen kuukauteen. Pääsuunnittelumoduuli määrittää tarjonnan (materiaalit) ja kapasiteetin (resurssit) tarpeen, joka vastaa nykyistä kysyntää (nettovaatimukset). Useimmissa yrityksissä tämä on laajennettu käsittämään pisin kumulatiivinen läpimenoaika, jonka aikana tuotteet vastaanotetaan.

## <a name="learning-map"></a>Oppimiskartta

Seuraavassa oppimiskartassa on esillä tärkeitä käsitteitä ja tehtäviä, joista pääsuunnittelumoduulin kehys koostuu. Opi käyttämään moduulia [Pikalinkit](#quick-links)-osion linkeistä.

[![Pääsuunnittelun oppimiskartta](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Pikalinkit

|      |   |
|------|---|
|        [Pääsuunnitelmat](master-plans.md)       |     [Rajoitetun suunnitelman luominen](./tasks/constrained-plan.md)  |
| [Oheistuotteiden materiaalisuunnitelman luominen](./tasks/create-material-plan-co-products.md)   |  [Pääsuunnittelu ja multisite-toiminnot](master-plan-multisite-functionality.md)  |
| [Konsernin sisäisen suunnitelman luominen](./tasks/create-intercompany-plan.md) | [Kysynnän ennustepalveluiden yleiskatsaus](introduction-demand-forecasting.md)  | 
|[Vähennysavaimet](reduction-keys.md)| [Pääsuunnittelua koskevat tärkeät seikat](https://mbspartner.microsoft.com/AX/CourseOverview/1275) (eLearning) (vaatii CustomerSource-tilin)     |
|  [Prosessivalmistuksen pääsuunnittelu](https://mbspartner.microsoft.com/D365E/CourseOverview/1514) (eLearning) (vaatii CustomerSource-tilin) | [Konsernin sisäinen pääsuunnittelu](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (eLearning) (vaatii CustomerSource-tilin)|
                                  
## <a name="additional-resources"></a>Lisäresurssit

### <a name="roadmaps"></a>Tiekartat
[Microsoft Dynamics 365 -ohjesivustolla](https://roadmap.dynamics.com/) on lisätietoja julkaistuista ja kehitteillä olevista uusista toiminnoista.

### <a name="blogs"></a>Blogit
Pääsuunnittelua sekä muita ratkaisuja koskevia mielipiteitä, uutisia ja muita tietoja löytyy kohdista [Dynamics AX:n valmistuksen tutkimus- ja kehitysryhmän blogi](https://blogs.msdn.microsoft.com/axmfg) ja [Dynamics AX:n toimitusketjun hallinnan tutkimus- ja kehitysryhmän blogi](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Tehtäväoppaat
Finance and Operationsin tehtäväoppaissa on lisäohjeita. Voit avata tehtäväoppaan napsauttamalla **Ohje**-painiketta millä tahansa sivulla.

### <a name="webinars"></a>Verkkoseminaarit
[Azuren koneoppimisen käyttäminen kysynnän ennusteessa](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Teknisen konferenssin tallenteet
-  [Kysynnän ennustetoimintojen laajentaminen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Pääsuunnittelu – vihjeitä suorituskyvyn vianmääritykseen](https://youtu.be/7v8BPmEs9Dg)
-  [Apua! Tarvesuunnittelu toimii hitaasti.](https://youtu.be/RLXybx20B5o)




