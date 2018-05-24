---
title: Viiveet
description: "Tässä artikkelissa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a>Viiveet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.

Pääsuunnittelu voi laskea tapahtumalle aikaisimman täyttymispäivämäärän läpimenoaikojen, materiaalin saatavuuden ja suunnittelun erilaisten parametrien perusteella. 

Jos pääsuunnittelu laskee tilauspäivämäärän, joka on aiempi kuin kuluva päivämäärä, tilausta ei voi täyttää ajoissa. Tämän vuoksi tilaus viivästyy. Tässä tapauksessa pääsuunnittelu suunnittelee tilauksen edelleen kuluvasta päivämäärästä ja sisällyttää läpimenoajat. Läpimenoajat lasketaan alatason osanimikkeistä alkaen. Tämän jälkeen tilaukselle määritetään viivästyspäivä. Viivästyspäivä on nykyisiin tietoihin perustuva realistinen eräpäivä. Pääsuunnittelu laskee myös viivästymispäivien määrän. 

Joissakin tilanteissa viivästyspäivää ei välttämättä käytetä. Näin voi käydä esimerkiksi silloin, kun käyttäjät tietävät voivansa jouduttaa läpimenoaikoja valitsemalla vaihtoehtoisen toimitustavan. 

Voit määrittää kattavuusryhmän viivästysten laskentatavat. Voit liittää kattavuusryhmän nimikkeeseen myöhemmin. 

**Pääsuunnittelun parametrit** -sivulla voit määrittää viivästymisten laskennan aloitusajan. Jos tilaus täyttyy tämän jälkeen, tilauksen viivästyspäivään lisätään yksi päivä. 

**Huomautus:** Aiemmissa versioissa laskettuja viiveitä kutsuttiin *viivästyssanomiksi*, viivästyspäivää *lasketuksi viivästyspäiväksi* ja viivästynyttä tapahtumaa *tulevaisuuteen määritetyksi tapahtumaksi*.

<a name="additional-resources"></a>Lisäresurssit
--------

[Kattavuusasetukset](coverage-settings.md)




