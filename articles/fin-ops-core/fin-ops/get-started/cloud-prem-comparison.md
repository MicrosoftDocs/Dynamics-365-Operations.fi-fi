---
title: Pilvipalvelun ja paikallisten ominaisuuksien vertailu
description: Tässä aiheessa kerrotaan, mitkä ominaisuudet ovat tuettuja pilvipalvelussa ja paikallisessa asennuksessa.
author: sericks007
manager: AnnBe
ms.date: 10/11/2019
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
ms.openlocfilehash: 8fa5ff0de4e97d5dc178581f721f3a6ea72fc974
ms.sourcegitcommit: 70c6257bd6833de3e8de34d9a7561088194e59cc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/11/2019
ms.locfileid: "2573927"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Pilvipalvelun ja paikallisten ominaisuuksien vertailu

[!include [banner](../includes/banner.md)]

Tässä aiheessa esitetään vertailu pilvessä ja paikan päällä käytettävissä olevien ominaisuuksien välillä seuraavien sovellusten osalta:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Retail](cloud-prem-comparison.md#dynamics-365-retail)
- [Dynamics 365 Talent](cloud-prem-comparison.md#dynamics-365-talent)

Mukana on tietoja myös [kehitys- ja hallintaominaisuuksista](cloud-prem-comparison.md#development-and-administration-features).

Seuraavissa taulukoissa luetellaan sovellusalueet. Pilvipalvelun ja paikallisen asennuksen tuki on lueteltu ominaisuudelle kokonaisuutena. Missä erityisominaisuudet vaihtelevat alueella yleisesti, ominaisuudet luetellaan erillisillä riveillä Ominaisuus-sarakkeessa.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Alue**             | **Ominaisuus**                | **Pilvi** | **Paikallinen** |
|---------------------|-----------------------------|-----------|-----------------|
| Yhteensopivuus ja sertifiointi        |                                                                                           | Kyllä       | Kyllä             |
|                                      | SOC 1 Type 1 -sertifikaatti                                                                | Kyllä       | Ei              |
| Tietojen hallinta ja integraatio      |                                                                                           | Kyllä       | Kyllä             |
|                                      | Määritysperustainen laajennus                                                            | Kyllä       | En              |
|                                      | Tietojen vienti omaan tietovarastoon                                                    | Kyllä       | Kyllä             |
|                                      | Lisäpäivitysten vienti tietoyksikköön                                 | Kyllä       | En              |
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

## <a name="dynamics-365-retail"></a>Dynamics 365 Retail 

Lisätietoja paikallisissa ympäristöissä käytettävissä olevista Retail-ominaisuuksista on kohdassa [Paikallisten ympäristöjen Retail-ominaisuudet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/PeterRFriis-patch-1/articles/retail/retail-onprem.md).

## <a name="dynamics-365-talent"></a>Dynamics 365 Talent 

| **Alue**         | **Ominaisuus**         | **Pilvi** | **Paikallinen** |
|------------------|---------------------|-----------|-----------------|
| Kaikki Talent-alueet | Kaikki Talent-ominaisuudet | Kyllä       | Ei              |

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

