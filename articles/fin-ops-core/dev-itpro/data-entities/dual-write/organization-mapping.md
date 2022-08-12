---
title: Organisaatiohierarkia Dataversessa
description: Tässä artikkelissa käsitellään organisaation tietojen integraatiota talous- ja toimintosovellusten sekä Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f900637855bee3e21916652a373c683e6bf1392
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112015"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisaatiohierarkia Dataversessa

[!include [banner](../../includes/banner.md)]



Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta. Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.

Vaikka Dataversessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä. Organisaatiohierarkian tietorakenne lisätään Dataverse -integroinnin osana Dataverseen.

## <a name="data-flow"></a>Tietojen virtaus

Liiketoiminnan ekosysteemillä, joka koostuu talous- ja toimintosovelluksista sekä Dataversesta, on jatkossakin organisaatiohierarkia. Tämä organisaatiohierarkia perustuu talous- ja toimintosovelluksiin, mutta se näkyy Dataversessa tiedon jakamista ja laajennettavuutta varten. Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Dataversessa yksisuuntaisena tiedonkulkuna talous- ja toimintosovelluksista Dataverseen.

![Arkkitehtuurikuva.](media/dual-write-data-flow.png)

Organisaatiohierarkian taulukoiden yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin talous- ja toimintosovelluksista Dataverseen.

## <a name="templates"></a>Mallit

Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita. Voit määrittää seuraavan tyyppisiä sisäisiä organisaatioita: yritysten toimintayksiköt ja ryhmiä. Kuten seuraavassa taulukossa näkyy, luodaan taulumääritysten kokoelma, jonka avulla synkronoidaan yritykset, toimintayksiköt ja niihin liittyvät hierarkiatiedot.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset     | Kuvaus
-----------------------|--------------------------------|---
[Oikeushenkilöt](mapping-reference.md#102) | cdm_companies | 
[Oikeushenkilöt](mapping-reference.md#142) | msdyn_internalorganizations |
[Toimintayksikkö](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisaatiohierarkia – julkaistu](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Tässä mallissa on yksisuuntainen Organisaatiohierarkia julkaistu -taulukon synkronointi.
[Organisaatiohierarkian tarkoitukset](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -taulukon synkronointi.
[Organisaatiohierarkian tyyppi](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Tässä mallissa on yksisuuntainen Organisaatiohierarkiatyyppi-taulukon synkronointi.

## <a name="internal-organization"></a>Sisäinen organisaatio

Sisäisen organisaation tiedot ovat Dataversessa peräisin kahdesta taulusta: **Toimintoyksikkö** ja **Yritykset**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

