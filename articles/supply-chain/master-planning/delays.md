---
title: Viiveet
description: Tässä artikkelissa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a87b19732f413aa2844101f76dea83535da86599
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "359609"
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



