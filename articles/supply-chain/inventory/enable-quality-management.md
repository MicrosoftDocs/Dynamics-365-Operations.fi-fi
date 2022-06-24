---
title: Ota käyttöön laadun ja määrityksistä poikkeamisen hallinta
description: Tässä artikkelissa on yhteenveto laadun ja määrityksistä poikkeamisen hallinnan ominaisuuksien määritys- ja konfigurointiprosessista Microsoft Dynamics 365 Supply Chain Managementissa.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66229e3692e87f774c553eae955794330602598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874040"
---
# <a name="enable-quality-and-nonconformance-management"></a>Ota käyttöön laadun ja määrityksistä poikkeamisen hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yhteenveto laadun ja määrityksistä poikkeamisen hallinnan ominaisuuksien määritys- ja konfigurointiprosessista Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön

Ota laadunhallinta käyttöön järjestelmässä noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit**.
1. Määritä **Laadunhallinta**-välilehdessä **Käytä laadunhallintaa** -asetukseksi *Kyllä*.
1. Syötä työn hinta paikallisena valuuttana **Tuntihinta**-kenttään. Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan. Tuntihinta ja lasketut kustannukset ovat määrityksistä poikkeamisen viitetietoja. Ne eivät vaikuta muihin toimintoihin.
1. Valitse **Raportin asetukset**.
1. Lisää eri raporttityypeille uusia rivejä ja valitse kussakin raportissa käytettävä asiakirjatyyppi.
1. Sulje sivu.
1. Sulje sivu.

## <a name="quality-management-configuration-process"></a>Laadunhallinnan määritysprosessi

Ennen kuin voit aloittaa laadunhallintaominaisuuksien käytön ja luoda laatutilauksia, sinun on määritettävä järjestelmä ja edellytykset. Tässä on luettelo vaiheista, joita tarvitaan laadunhallinnan konfiguroinnissa.

1. [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](#enable-qm).
1. Valinnainen: [Testin mittavälineiden määrittäminen](quality-test-instruments.md).
1. [Testien määrittäminen](quality-tests.md).
1. [Testimuuttujien ja tulosten määrittäminen](quality-test-variables.md).
1. [Testiryhmien määrittäminen](quality-test-groups.md).
1. Valinnainen: [Laaturyhmien määrittäminen ja linkittäminen tuotteisiin](quality-groups.md).
1. Valinnainen: [Laatuliitosten määrittäminen](quality-associations.md).

Kun määrittäminen on valmis, voit aloittaa laatutilausten luomisen ja käsittelemisen. Lisätietoja laatutilausten luomisesta ja käyttämisestä on kohdassa [Laatutilaukset](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Määrityksistä poikkeamisen hallinnan määritysprosessi

Ennen kuin voit aloittaa määrityksistä poikkeamisen hallinnan ominaisuuksien käytön ja luoda määrityksistä poikkeamisia, sinun on määritettävä järjestelmä ja edellytykset. Tässä on luettelo vaiheista, joita tarvitaan määrityksistä poikkeamisen hallinnan konfiguroinnissa.

1. [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](#enable-qm).
1. [Määrityksistä poikkeamisia hyväksyvien työntekijöiden määrittäminen](quality-responsible-workers.md).
1. [Ongelmatyyppien määrittäminen](quality-problem-types.md).
1. [Karanteenivyöhykkeiden määrittäminen](quality-quarantine-zones.md).
1. [Diagnostiikkatyyppien määrittäminen](quality-diagnostic-types.md).
1. [Operaatioiden määrittäminen](quality-operations.md).
1. Valinnainen: [Laatukulujen määrittäminen](quality-charges.md).

Kun määrittäminen on valmis, voit aloittaa määrityksistä poikkeamisten luomisen ja käsittelemisen. Lisätietoja määrityksistä poikkeamisten luonnista ja käyttämisestä on kohdassa [Määrityksistä poikkeamisten luonti ja käsittely](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
