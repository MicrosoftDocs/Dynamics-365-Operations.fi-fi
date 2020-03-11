---
title: Pilvipalvelun ja paikallisten ominaisuuksien vertailu
description: Tässä aiheessa kerrotaan, mitkä ominaisuudet ovat tuettuja pilvipalvelussa ja paikallisessa asennuksessa.
author: sericks007
manager: AnnBe
ms.date: 02/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: a918d9fa1ad7ed5adcbb1d056bb8cc3306507aec
ms.sourcegitcommit: 8ff2413b6cb504d2b36fce2bb50441b2e690330e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/24/2020
ms.locfileid: "3081967"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Pilvipalvelun ja paikallisten ominaisuuksien vertailu

[!include [banner](../includes/banner.md)]

Tässä aiheessa esitetään vertailu pilvessä ja paikan päällä käytettävissä olevien ominaisuuksien välillä seuraavien sovellusten osalta:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Mukana on tietoja myös [kehitys- ja hallintaominaisuuksista](cloud-prem-comparison.md#development-and-administration-features).

Seuraavissa taulukoissa luetellaan sovellusalueet. Pilvipalvelun ja paikallisen asennuksen tuki on lueteltu ominaisuudelle kokonaisuutena. Missä erityisominaisuudet vaihtelevat alueella yleisesti, ominaisuudet luetellaan erillisillä riveillä Ominaisuus-sarakkeessa.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Alue**             | **Ominaisuus**                | **Pilvi** | **Paikallinen** |
|---------------------|-----------------------------|-----------|-----------------|
| Yhteensopivuus ja sertifiointi        |                                                                                           | Kyllä       | Kyllä             |
|                                      | SOC 1 Type 1 -sertifikaatti                                                                | Kyllä       | Ei              |
| Tietojen hallinta ja integraatio      |                                                                                           | Kyllä       | Kyllä             
|                                      | Tietojen vienti omaan tietovarastoon                                                    | Kyllä       | Kyllä             |
|                                      | Lisäpäivitysten vienti tietoyksikköön                                 | Kyllä       | Kyllä              |
|                                      | Tietojen integroinnit                                                                         | Kyllä       | Kyllä             |
| Tiedoston hallinta                  |                                                                                           | Kyllä       | Kyllä             |
| Taloushallinto                 |                                                                                           | Kyllä       | Kyllä             |
| Ohje                                 |                                                                                           | Kyllä       | En              |
| Henkilöstöhallinto                      |                                                                                           | Kyllä       | Kyllä             |
| Tiedot                         |                                                                                           | Kyllä       | Kyllä             |
|                                      | Sähköinen raportointi (ER)                                                                 | Kyllä       | Kyllä             |
|                                      | ER: Integrointi LCS:n kanssa                                                                  | Kyllä       | Ei              |
|                                      | ER: Integrointi SharePointin kanssa                                                           | Kyllä       | Ei              |
|                                      | ER: Integrointi Regulatory Configuration Services (RCS) -palvelun kanssa                              | Kyllä       | Ei              |
|                                      | ER: Käyttää paikallista tiedostojärjestelmää ER-kokoonpanojen tallennuksena, joka on käytettävissä ER-tietovarastojen kautta | Ei        | Kyllä             |
|                                      | PowerBI.com-integrointi                                                              | Kyllä       | Ei              |
|                                      | Integrointi PowerBI Desktop:n kanssa                                                          | Ei        | Kyllä             |
|                                      | Analyysityötilat                                                                     | Kyllä       | Ei              |
|                                      | Älykkäät liiketoimintaprosessit: Suositukset                                             | Kyllä       | Nro              |
|                                      | Power BI -raporttien sisällön tuottaminen ODatalla Power BI -työpöydän tai Excel PowerQuery -työkalujen avulla    | Kyllä       | Nro              |
|                                      | SQL Server Reporting Services (SSRS) tukee skaalautumista                                 | Kyllä       | Ei              |
|                                      | Telemetria siirretään pilveen                                                   | Kyllä       | Ei              |
| Käyttöikäpalvelut                   |                                                                                           | Kyllä       | Kyllä             |
|                                      | Konfiguroitavat liiketoimintaprosessit                                                           | Kyllä       | Ei              |
| Lokalisoinnit                        |                                                                                           | Kyllä       | Kyllä             |
| Mobiilisovellus, -työtilat ja -ympäristö |                                                                                           | Kyllä       | Kyllä             |
| Office-integraatio                   |                                                                                           | Kyllä       | Kyllä             |
| Organisaation hallinto          |                                                                                           | Kyllä       | Kyllä             |
| Palkanlaskenta                              |                                                                                           | Kyllä       | Kyllä             |
|                                      | Suoratalletus                                                                            | Kyllä       | Ei              |
| Projektinhallinta ja kirjanpito    |                                                                                           | Kyllä       | Kyllä             |
| Suojaus                             |                                                                                           | Kyllä       | Kyllä             |
| Huoltohallinta                   |                                                                                           | Kyllä       | Kyllä             |
| WWW-asiakasohjelma                           |                                                                                           | Kyllä       | Kyllä             |
|                                      | Tehtävien tallennustoiminto - tallenna tai lataa tehtävätallenteita BPM-kirjastosta                         | Kyllä       | En              |
| Tuki                              |                                                                                           | Kyllä       | Kyllä             |
|                                      | Nopea tuki Ohje ja tuki -valikon kautta                                             | Kyllä       | Ei              |
|                                      | Liiketoimintatapahtumat                                                                           | Kyllä       | Kyllä (internet-yhteys on pakollinen tai mukautetut päätepisteet on otettava käyttöön liiketoimintatapahtumien lähettämistä ja vastaanottamista varten intranetissä)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Alue**                | **Ominaisuus**             | **Pilvi** | **Paikallinen** |
|-------------------------|-------------------|-----------|-----------------|
| Yhteensopivuus ja sertifiointi        |                                                                                           | Kyllä       | Kyllä             |
|                                      | SOC 1 Type 1 -sertifikaatti                                                                | Kyllä       | Nro              |
| Kustannuslaskenta                      |                                                                                           | Kyllä       | Kyllä             |
|                                      | Kustannuslaskennan Power BI -sisältöpaketti                                                 | Kyllä       | Nro              |
|                                      | Kustannuslaskennan mobiilityötila                                                  | Kyllä       | Nro              |
| Kustannushintojen hallinta                      |                                                                                           | Kyllä       | Kyllä             |
|                                      | Kustannushallinnan Power BI -sisältöpaketti                                                 | Kyllä       | Nro              |
| Tietojen hallinta ja integraatio      |                                                                                           | Kyllä       | Kyllä             |
|                                      | Määritysperustainen laajennus                                                            | Kyllä       | En              |
|                                      | Tietojen vienti omaan tietovarastoon                                                    | Kyllä       | Kyllä             |
|                                      | Lisäpäivitysten vienti tietoyksikköön                                 | Kyllä       | Ei              |
|                                      | Tietojen integroinnit                                                                         | Kyllä       | Kyllä             |
| Tiedoston hallinta                  |                                                                                           | Kyllä       | Kyllä             |
| Ohje                                 |                                                                                           | Kyllä       | Ei              |
| Tiedot                         |                                                                                           | Kyllä       | Kyllä             |
|                                      | Sähköinen raportointi (ER)                                                                 | Kyllä       | Kyllä             |
|                                      | ER: Integrointi LCS:n kanssa                                                                  | Kyllä       | Ei              |
|                                      | ER: Integrointi SharePointin kanssa                                                           | Kyllä       | Ei              |
|                                      | ER: Integrointi Regulatory Configuration Services (RCS) -palvelun kanssa                              | Kyllä       | Ei              |
|                                      | ER: Käyttää paikallista tiedostojärjestelmää ER-kokoonpanojen tallennuksena, joka on käytettävissä ER-tietovarastojen kautta | Ei        | Kyllä             |
|                                      | PowerBI.com-integrointi                                                              | Kyllä       | Ei              |
|                                      | Integrointi PowerBI Desktop:n kanssa                                                          | Ei        | Kyllä             |
|                                      | Analyysityötilat                                                                     | Kyllä       | Ei              |
|                                      | Älykkäät liiketoimintaprosessit: Suositukset                                             | Kyllä       | Nro              |
|                                      | Power BI -raporttien sisällön tuottaminen ODatalla Power BI -työpöydän tai Excel PowerQuery -työkalujen avulla    | Kyllä       | Nro              |
|                                      | SQL Server Reporting Services (SSRS) tukee skaalautumista                                 | Kyllä       | En              |
|                                      | Telemetria siirretään pilveen                                                   | Kyllä       | En              |
| Varastoinninhallinta                 |                                                                                           | Kyllä       | Kyllä             |
| Käyttöikäpalvelut                   |                                                                                           | Kyllä       | Kyllä             |
|                                      | Konfiguroitavat liiketoimintaprosessit                                                           | Kyllä       | En              |
| Lokalisoinnit                        |                                                                                           | Kyllä       | Kyllä             |
| Valmistus                        |                                                                                           | Kyllä       | Kyllä             |
| Pääsuunnittelu ja ennusteet      |                                                                                           | Kyllä       | Kyllä             |
| Mobiilisovellus, -työtilat ja -ympäristö |                                                                                           | Kyllä       | Kyllä             |
| Office-integraatio                   |                                                                                           | Kyllä       | Kyllä             |
| Organisaation hallinto          |                                                                                           | Kyllä       | Kyllä             |
| Hankinta             |                                                                                           | Kyllä       | Kyllä             |
|                                      | Siirto ulkoiseen luetteloon ostoehdotuksesta                                   | Kyllä       | Nro              |
|                                      | Osto- ja kulutusanalyysin Power BI -raportit                                                  | Kyllä       | Nro              |
| Tuotetietojen hallinta       |                                                                                           | Kyllä       | Kyllä             |
| Päätuotetiedot                  |                                                                                           | Kyllä       | Kyllä             |
| Tuotanto                           |                                                                                           | Kyllä       | Kyllä             |
|                                      | Tuotannon suorituskyvyn Power BI -raportit                                                   | Kyllä       | Nro              |
| Projektinhallinta ja kirjanpito    |                                                                                           | Kyllä       | Kyllä             |
| Myynti                                |                                                                                           | Kyllä       | Kyllä             |
|                                      | Myynnin ja tuottavuuden suorituskyvyn Power BI -raportit                                      | Kyllä       | Nro              |
| Suojaus                             |                                                                                           | Kyllä       | Kyllä             |
| Huoltohallinta                   |                                                                                           | Kyllä       | Kyllä             |
| Toimitusketjun hallinta              |                                                                                           | Kyllä       | Kyllä             |
| Kuljetustenhallinta            |                                                                                           | Kyllä       | Kyllä             |
| Toimittajayhteistyö                 |                                                                                           | Kyllä       | En              |
| Varastonhallinta                   |                                                                                           | Kyllä       | Kyllä             |
|                                      | Varaston mobiilisovellus                                                                      | Kyllä       | Kyllä             |
|                                      | Varastoinnin Power BI -raportit                                                              | Kyllä       | Nro              |
| WWW-asiakasohjelma                           |                                                                                           | Kyllä       | Kyllä             |
|                                      | Tehtävien tallennustoiminto - tallenna tai lataa tehtävätallenteita BPM-kirjastosta                         | Kyllä       | En              |
| Tuki                              |                                                                                           | Kyllä       | Kyllä             |
|                                      | Nopea tuki Ohje ja tuki -valikon kautta                                             | Kyllä       | Ei              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Lisätietoja paikallisissa ympäristöissä käytettävissä olevista ominaisuuksista on kohdassa [Paikallisten ympäristöjen Commerce-ominaisuudet](../../../retail/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Alue**         | **Ominaisuus**         | **Pilvi** | **Paikallinen** |
|------------------|---------------------|-----------|-----------------|
| Kaikki henkilöstöhallinnon alueet | Kaikki henkilöstöhallinnon toiminnot | Kyllä       | Ei              |

## <a name="development-and-administration-features"></a>Kehitys- ja hallintaominaisuudet

| **Alue**                   | **Ominaisuus**                               | **Pilvi** | **Paikallinen** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Muodostus ja testaus             |                                           | Kyllä       | Kyllä             |
| Laajennettavuus              |                                           | Kyllä       | Kyllä             |
| Seuranta ja telemetria   |                                           | Kyllä       | Kyllä             |
| Ympäristöyhteensopivuus     |                                           | Kyllä       | Kyllä             |
| Päivitetään                  |                                           | Kyllä       | Kyllä             |
|                            | Päivitysympäristöt                    | Kyllä       | En              |
| Jäljityksen jäsennin ja PerfTimer |                                           | Kyllä       | En              |
| Päivitä                    |                                           | Kyllä       | Kyllä             |
|                            | Päivitä                                   | Kyllä       | Nro              |
|                            | Aiempien versioiden päivittäminen ja tuki | Kyllä       | Ei              |
| Visual Studion kehitys  |                                           | Kyllä       | Kyllä             |

