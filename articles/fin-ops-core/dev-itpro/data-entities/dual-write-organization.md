---
title: Organisaatiohierarkia Common Data Servicessa
description: Tässä aiheessa kuvataan organisaation tietojen integraatiota Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182022"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organisaatiohierarkia Common Data Servicessa

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Koska Dynamics 365 Finance on talousjärjestelmä, *organisaatio* on keskeinen käsite ja järjestelmän asennusohjelma alkaa organisaatiohierarkian konfiguraatiosta. Yrityksen taloustietoja voidaan sitten seurata organisaatiotasolla ja millä tahansa organisaatiohierarkian tasolla.

Vaikka Common Data Servicessa ei ole käsitettä organisaatiohierarkia, siinä on joitakin käsitteitä, kuten myyntituoton kokonaismäärä. Organisaatiohierarkian tietorakenne lisätään Common Data Service -integroinnin osana Common Data Serviceen.

## <a name="data-flow"></a>Tietojen virtaus

Liiketoiminnan ekosysteemillä, joka koostuu Finance and Operations -sovelluksesta ja Common Data Servicesta, on jatkossakin organisaatiohierarkia. Tämä organisaatiohierarkia perustuu Finance and Operations -sovelluksiin, mutta se näkyy Common Data Servicessa tiedon jakamista ja laajennettavuutta varten. Seuraavassa kuvassa näkyy organisaatiohierarkian tiedot, jotka näkyvät Common Data Servicessa yksisuuntaisena tiedonkulkuna Finance and Operations- sovelluksista Common Data Serviceen.

![Arkkitehtuurikuva](media/dual-write-data-flow.png)

## <a name="templates"></a>Mallit

Organisaatiohierarkian entiteettien yhdistämismääritykset ovat käytettävissä yksisuuntaiseen tietojen synkronointiin Finance and Operations -sovelluksista Common Data Serviceen.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Sisäinen organisaatiohierarkian tarkoitus

Tässä mallissa on yksisuuntainen Organisaatiohierarkian tarkoitus -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Sisäinen organisaatiohierarkian tyyppi

Tässä mallissa on yksisuuntainen Organisaatiohierarkian tyyppi -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.

<!-- ![architecture image](media/dual-write-type.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Sisäinen organisaatiohierarkia

Tässä mallissa on yksisuuntainen Julkaistu organisaatiohierarkia -yksikön synkronointi Finance and Operationsista muihin Dynamics 365 -sovelluksiin.

<!-- ![architecture image](media/dual-write-organization.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Sisäinen organisaatio

Sisäisen organisaation tiedot ovat Common Data Servicessa peräisin kahdesta yksiköstä: **toimintayksikkö** ja **yritykset**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Toimintayksikkö

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NIMI | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Oikeushenkilö

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NIMI | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
none | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Yritys 

Sisältää oikeushenkilön (yrityksen) kaksisuuntaisen synkronoinnin Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä.

<!-- ![architecture image](media/dual-write-company.png) -->

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
NIMI | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
