---
title: Organisaatiohierarkia Dataversessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota taloushallinnon ja toimintojen sovellusten ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: afc1b5996667835c460f467526493380aa2d6403
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062083"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisaatiohierarkia Dataversessa

[!include [banner](../../includes/banner.md)]



Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta. Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.

Vaikka Dataversessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä. Organisaatiohierarkian tietorakenne lisätään Dataverse -integroinnin osana Dataverseen.

## <a name="data-flow"></a>Tietojen virtaus

Liiketoiminnan ekosysteemillä, joka koostuu taloushallinnon ja toimintojen sovelluksesta ja Dataversesta, on jatkossakin organisaatiohierarkia. Tämä organisaatiohierarkia perustuu taloushallinnon ja toimintojen sovelluksiin, mutta se näkyy Dataversessa tiedon jakamista ja laajennettavuutta varten. Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Dataversessa yksisuuntaisena tiedonkulkuna Finance and Operations- sovelluksista Dataverseen.

![Arkkitehtuurikuva.](media/dual-write-data-flow.png)

Organisaatiohierarkian taulukoiden yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin taloushallinnon ja toimintojen sovelluksista Dataverseen.

## <a name="templates"></a>Mallit

Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot. Seuraava taulukko osoittaa, miten taulukarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
-----------------------|--------------------------------|---
[Oikeushenkilöt](mapping-reference.md#102) | cdm_companies | Sisältää yrityksen (yhtiön) kaksisuuntaisen synkronoinnin.
[Oikeushenkilöt](mapping-reference.md#142) | msdyn_internalorganizations |
[Toimintayksikkö](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisaatiohierarkia – julkaistu](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Tässä mallissa on yksisuuntainen Organisaatiohierarkia julkaistu -taulukon synkronointi.
[Organisaatiohierarkian tarkoitukset](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -taulukon synkronointi.
[Organisaatiohierarkian tyyppi](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Tässä mallissa on yksisuuntainen Organisaatiohierarkiatyyppi-taulukon synkronointi.

## <a name="internal-organization"></a>Sisäinen organisaatio

Sisäisen organisaation tiedot ovat Dataversessa peräisin kahdesta taulusta: **Toimintoyksikkö** ja **Yritykset**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
