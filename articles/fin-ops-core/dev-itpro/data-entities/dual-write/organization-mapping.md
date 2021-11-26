---
title: Organisaatiohierarkia Dataversessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota Finance and Operations -sovellusten ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7ef3a11817d60343503c80d89493262711524b1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782305"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisaatiohierarkia Dataversessa

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta. Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.

Vaikka Dataversessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä. Organisaatiohierarkian tietorakenne lisätään Dataverse -integroinnin osana Dataverseen.

## <a name="data-flow"></a>Tietojen virtaus

Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operations -sovelluksesta ja Dataversesta, on jatkossakin organisaatiohierarkia. Tämä organisaatiohierarkia perustuu Finance and Operations -sovelluksiin, mutta se näkyy Dataversessä tiedon jakamista ja laajennettavuutta varten. Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Dataversessä yksisuuntaisena tiedonkulkuna Finance and Operations -sovelluksista Dataverseen.

![Arkkitehtuurikuva.](media/dual-write-data-flow.png)

Organisaatiohierarkian taulujen yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operations -sovelluksista Dataverseen.

## <a name="templates"></a>Mallit

Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot. Seuraava taulukko osoittaa, miten taulukarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.

Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
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
