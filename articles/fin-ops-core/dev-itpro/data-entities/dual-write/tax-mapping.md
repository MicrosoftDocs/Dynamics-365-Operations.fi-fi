---
title: Integroitu vero
description: Tässä aiheessa kuvataan verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560334"
---
# <a name="integrated-tax"></a>Integroitu vero

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.

## <a name="templates"></a>Mallit

Verotiedot sisältävät taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Dynamics 365:n mallipohjaiset sovellukset | kuvaus |
-------------------------|---------------------------------|----|
Nimikkeen arvonlisäveroryhmä | msdyn_taxitemgroups |
Alv-viranomaiset | msdyn_taxauthorities |
Arvonlisäveron verovapauskoodin yksikkö CDS:lle | msdyn_taxexemptcodes |
Arvonlisäveroryhmät | msdyn_taxgroups |
Arvonlisäveron kirjanpidon kirjausryhmät V2 | msdyn_taxpostinggroups |
Ennakonpidätyskoodit | msdyn_withholdingtaxcodes |
Ennakonpidätysryhmät | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]