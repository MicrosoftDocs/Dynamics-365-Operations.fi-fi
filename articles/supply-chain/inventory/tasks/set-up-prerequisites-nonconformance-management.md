--- 
title: "Määritä määrityksistä poikkeamisen hallinnan edellytykset"
description: "Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Määritä määrityksistä poikkeamisen hallinnan edellytykset

[!include [task guide banner](../../includes/task-guide-banner.md)]

Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit. Määrityksistä poikkeaminen tarkoittaa menettelyä tai nimikettä, jolla on laatuongelma, jossa kuvaavat tiedot sisältävät ongelman lähteen ja tyypin. Menettely käyttää USMF-yrityksen demotietoja. Tämän menettelyn suorittaa yleensä laatupäällikkö.


## <a name="enable-quality-management-processes-within-the-company"></a>Ota laadunvalvontaprosessit käyttöön yrityksessä
1. Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.
2. Valitse Laadunhallinta-välilehti.
3. Valitse Käytä laadunhallintaa -kentässä Kyllä.
    * Valitse tämä parametri ottaaksesi käyttöön yrityksen laadunhallintaprosessit.  
4. Syötä Tuntihinta-kenttään haluamasi luku.
    * Syötä työn hinta paikallisena valuuttana Tuntihinta-kenttään. Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan. Tuntihinta ja lasketut kustannukset ovat poikkeaman viitetietoja, eivätkä ne vaikuta muihin toimintoihin.  
5. Valitse Raportin asetukset.
    * Tällä sivulla voit määrittää erityyppisissä laadunhallintaraporteissa käytettävät laaturaporttien huomautustyypit.  
6. Sulje sivu.
7. Sulje sivu.

## <a name="enable-user-for-nonconformance-processing"></a>Salli käyttäjälle määrityksistä poikkeamisen käsittely
1. Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.
    * Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla. Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.  
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Nimi-kenttää arvolla "Riku".
    * Paikanna määrityksistä poikkeamiset hyväksyvä tai hylkäävä käyttäjä suodattimen avulla.  
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.  
4. Napsauta Käyttäjän asetukset.
5. Napsauta Asetukset-välilehteä.
6. Valitse Ota tiedoston käsittely käyttöön -kentän arvoksi Kyllä.
    * Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.  
7. Sulje sivu.
8. Sulje sivu.
9. Sulje sivu.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn diagnostiikkatyypit
1. Valitse Varastonhallinta > Asetukset > Laadunhallintaa > Diagnostiikan tyypit.
    * Määritä vianmääritystoimenpiteiden luokitus Vianmääritystyypit-sivulla. Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen, sen tekijän sekä halutun ja suunnitellun valmistumispäivämäärän.  
2. Valitse Uusi.
3. Kirjoita arvo Diagnostiikka-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Sulje sivu.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn laadun kulut
1. Valitse Varastonhallinta > Asetukset > Laadunhallinta > Laadun kulut.
    * Määritä määrityksistä poikkeamiseen liittyvien toimintojen kulujen luokittelu Laadun kulut -sivulla.  
2. Valitse Uusi.
3. Kirjoita Kulujen koodi -kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Sulje sivu.

## <a name="define-the-operations-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn toiminnot
1. Valitse Varastonhallinta > Asetukset > Laadunhallinta > Toiminnot.
    * Määritä Toiminnot-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten. Kun liität poikkeamaan toiminnon, voit määrittää tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista. Näitä tietoja käytetään perustana laskettaessa toiminnon arvioituja kustannuksia.  
2. Valitse Uusi.
3. Kirjoita arvo Toiminto-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Sulje sivu.

## <a name="define-problem-types-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn ongelmatyypit
1. Valitse Varastonhallinta > Asetukset > Laadunhallinta > Ongelmatyypit.
    * Määritä Ongelmatyypit-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä. Määrityksistä poikkeamisen tyypit ovat: Sisäinen, Asiakas, Toimittaja, Palvelupyyntö, Tuotanto ja Oheistuotteen tuotanto. Yksittäisen ongelmatyypin voi liittää useampaan määrityksistä poikkeamisen tyyppiin.  
2. Valitse Uusi.
3. Kirjoita arvo Ongelman tyyppi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Napsauta Määrityksistä poikkeamisen tyypit -kohtaa.
    * Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi Määrityksistä poikkeamisen tyypit -sivulla. Vikakoodia koskeva ongelmatyyppi voi esimerkiksi liittyä kaikkiin poikkeamatyyppeihin, kun taas asiakasvalituksia koskeva ongelmatyyppi voi liittyä vain asiakkaan ja huoltopyynnön poikkeamatyyppeihin.  
6. Valitse Uusi.
7. Merkitse valittu rivi luettelossa.
8. Valitse Määrityksistä poikkeamisen tyyppi -kentässä vaihtoehto.
9. Sulje sivu.
10. Sulje sivu.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Määritä määrityksistä poikkeamisen käsittelyn karanteenivyöhykkeet
1. Valitse Varastonhallinta > Asetukset > Laadunhallinta > Karanteenivyöhykkeet.
2. Valitse Uusi.
3. Kirjoita Karanteenivyöhyke-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Sulje sivu.


