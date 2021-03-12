---
title: Määritä määrityksistä poikkeamisen hallinnan edellytykset
description: Tämän ohjeaiheen avulla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961509"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Määritä määrityksistä poikkeamisen hallinnan edellytykset

[!include [banner](../../includes/banner.md)]

Tämän ohjeaiheen avulla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit. Määrityksistä poikkeaminen tarkoittaa menettelyä tai nimikettä, jolla on laatuongelma, jossa kuvaavat tiedot sisältävät ongelman lähteen ja tyypin. Menettely käyttää USMF-yrityksen demotietoja. Tämän menettelyn suorittaa yleensä laatupäällikkö.


## <a name="enable-quality-management-processes-within-the-company"></a>Ota laadunvalvontaprosessit käyttöön yrityksessä
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit**.
2. Valitse **Laadunhallinta**-välilehti.
3. Ota laadunhallintaprosessit käyttöön yrityksessäsi valitsemalla **Käytä laadunhallintaa** -kentässä **Kyllä**.
4. Syötä arvo paikallisena valuuttana **Tuntihinta**-kenttään. Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan. Tuntihinta ja lasketut kustannukset ovat poikkeaman viitetietoja, eivätkä ne vaikuta muihin toimintoihin.  
5. Valitse **Raportin asetukset** määrittääksesi erityyppisissä laadunhallintaraporteissa käytettävät laaturaporttien huomautustyypit.

## <a name="enable-user-for-nonconformance-processing"></a>Salli käyttäjälle määrityksistä poikkeamisen käsittely
1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**. 
2. Paikanna määrityksistä poikkeamiset hyväksyvä tai hylkäävä käyttäjä pikasuodattimen avulla. Voit esimerkiksi suodattaa **Nimi**-kenttää arvolla `Ricardo`. Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo **Käyttäjät**-sivulla. Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.  
3. Merkitse halutun tietueen rivi.
4. Valitse **Käyttäjäasetukset**.
5. Valitse **Asetukset**-välilehti.
6. Valitse **Ota tiedoston käsittely käyttöön** -kentän arvoksi **Kyllä**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn diagnostiikkatyypit
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Laadunhallinta > Diagnostiikan tyypit**. Määritä vianmääritystoimenpiteiden luokitus **Vianmääritystyypit**-sivulla. Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen, sen tekijän sekä halutun ja suunnitellun valmistumispäivämäärän.  
2. Valitse **Uusi**.
3. Kirjoita arvo **Diagnostiikka**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn laadun kulut
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Laadunhallinta > Laadun kulut**. Määritä määrityksistä poikkeamiseen liittyvien toimintojen kulujen luokittelu **Laadun kulut** -sivulla.  
2. Valitse **Uusi**.
3. Kirjoita **Kulujen koodi** -kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.

## <a name="define-the-operations-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn toiminnot
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Laadunhallinta > Toiminnot**. Määritä **Toiminnot**-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten. Kun liität poikkeamaan toiminnon, voit määrittää tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista. Näitä tietoja käytetään perustana laskettaessa toiminnon arvioituja kustannuksia.  
2. Valitse **Uusi**.
3. Kirjoita arvo **Toiminto**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.

## <a name="define-problem-types-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn ongelmatyypit
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Laadunhallinta > Ongelman tyypit**. Määritä **Ongelmatyypit**-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä. Määrityksistä poikkeamisen tyypit ovat: **Sisäinen**, **Asiakas**, **Toimittaja**, **Palvelupyyntö**, **Tuotanto** ja **Oheistuotteen tuotanto**. Yksittäisen ongelmatyypin voi liittää useampaan määrityksistä poikkeamisen tyyppiin.  
2. Valitse **Uusi**.
3. Kirjoita arvo **Ongelman tyyppi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Määrityksistä poikkeamisen tyypit**. Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi **Määrityksistä poikkeamisen tyypit** -sivulla. Vikakoodia koskeva ongelmatyyppi voi esimerkiksi liittyä kaikkiin poikkeamatyyppeihin, kun taas asiakasvalituksia koskeva ongelmatyyppi voi liittyä vain asiakkaan ja huoltopyynnön poikkeamatyyppeihin.  
6. Valitse **Uusi**.
7. Valitse uuden rivin **Määrityksistä poikkeamisen tyyppi** -kentässä vaihtoehto.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn karanteenivyöhykkeet
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Laadunhallinta > Karanteenivyöhykkeet**.
2. Valitse **Uusi**.
3. Kirjoita **Karanteenivyöhyke**-kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Sulje sivu.

