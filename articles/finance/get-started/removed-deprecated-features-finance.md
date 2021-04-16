---
title: Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.
author: roschlom
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 5a8f5dbc52eab78697de0d3a48d8cceb42c36540
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836910"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Financen version 10.0.17 poistetut tai vanhentuneet ominaisuudet

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-tietovarasto sähköisen raportoinnin konfiguraatioiden tallennusvaihtoehtona

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan Regulatory Configuration Service (RCS) -yleistietovarastolla. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Dynamics 365 Finance-, Supply Chain Management- ja Project Operations -tuotteet|
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme että Microsoft Dynamics Lifecycle Services (LCS) -tietovarastoa ei enää tueta 1.4.2022 alkaen sähköisen raportoinnin (ER) konfiguraatioiden tallennussäilönä. Uudet Microsoftin ER-konfiguraatiot julkaistaan yksinomaan yleisestä tietovarastosta ladattavaksi. Yleinen tietovarasto on käytettävissä Dynamics 365 -tuotteiden ja RCS:n kautta. Lisätietoja on kohdassa [ER-konfiguraatioiden tuonti RCS:stä](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Financen version 10.0.16 poistetut tai vanhentuneet ominaisuudet

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Sähköisen raportoinnin "ALV-ilmoitus (CZ)"- ja "Ohjausilmoituksen vienti (CZ)"-muodot – Tšekin tasavalta

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uusilla muodoilla |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 22.1.2022 alkaen suunnittelemme, että enää ei tueta sähköisen raportoinnin "ALV-ilmoitus (CZ)"- ja "Ohjausilmoituksen vienti (CZ)"-muotoja. Uudet ALV-ilmoitus, XML (CZ)-, ALV-ilmoitus, Excel (CZ)-, ALV-ohjausilmoitus, XML (CZ) -muodot tulevat käyttöön veroilmoitusmallissa. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>Belgian kirjanpidon tapahtumien vientimuoto (BE), sähköisen raportoinnin muoto ja vastaava kirjanpidon tapahtumien vienti -malli

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvattu uudella sähköisen raportoinnin muodolla SAF-T (Standard Audit File) -mallissa.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1.12.2021 jälkeen Belgian kirjanpidon tapahtumien vientimuoto (BE), sähköisen raportoinnin muoto ja vastaava kirjanpidon tapahtumien vienti -mallia ei enää tueta. SAF-T-mallissa esitellään uusi Kirjanpidon tietojen vienti (BE) -muoto yhdessä Kirjanpidon tietomallin yhdistämismääritys -muodon kanssa. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Yhdistyneen kuningaskunnan ALV 100 -raoprtti on SSRS-muodossa

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvattu uudella sähköisen raportoinnin muodolla - ALV-ilmoituksen Excel (UK) -muoto Veroilmoitusmalli-kohdassa.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1.12.2021 alkaen ALV-100-raporttia ei enää tueta SSRS-muodossa. Uusi ALV-ilmoituksen Excel (UK) -muoto Veroilmoitusmalli-kohdassa esiteltiin [MTD ALV -toiminto](../localizations/emea-gbr-mtd-vat-integration.md) -kohdassa. |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Financen version 10.0.15 poistetut tai vanhentuneet ominaisuudet

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11:n Dynamics 365 -tuki on vanhentunut

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Joulukuusta 2020 alkaen kaikkien Dynamics 365 -tuotteiden Microsoft Internet Explorer 11 -tuki vanhenee eikä Internet Explorer 11:tä tueta elokuun 2021 jälkeen.<br><br>Tämä vaikuttaa sellaisiin Dynamics 365 -tuotteita käyttäviin asiakkaisiin, jotka on suunniteltu käytettäviksi Internet Explorer 11 -liittymässä. Elokuun 2021 jälkeen Internet Explorer 11:tä ei tueta kyseisissä Dynamics 365 -tuotteissa. |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaiden kannattaa siirtyä Microsoft Edgeen.|
| **Tuotealueet, joihin vaikutetaan**         | Kaikki Dynamics 365 -tuotteet |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut. Internet Explorer 11:tä ei tueta elokuun 2021 jälkeen.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Financen version 10.0.12 poistetut tai vanhentuneet ominaisuudet

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Puolan SSRS-raportit, maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri - toimintojen viite PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ei lakisääteistä edellytystä.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä (Excel-muoto vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa - JPK_VDEK) |
| **Tuotealueet, joihin vaikutetaan**         | Sovellus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1.7.2021 jälkeen emme enää tue SSRS-raportteja: **Maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri – toimintojen viite PL-00014**. Excel-muodon esimerkki vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa (JPK_VDEK) otetaan sen sijaan käyttöön. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Financen version 10.0.11 poistetut tai vanhentuneet ominaisuudet

### <a name="norwegian-standard-main-accounts"></a>Norjan vakiopäätilit

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uudelleensuunnittelu  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä (sovelluskohtaiset parametrit korvattu ER-muodolla) |
| **Tuotealueet, joihin vaikutetaan**         | Sovellus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1. huhtikuuta 2021 mennessä emme enää tue vakiopäätileihin liittyviä toimintoja: viitekenttä, liittyvä taulu, tietoyksikkö. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Financen version 10.0.7 poistetut tai vanhentuneet ominaisuudet

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Siirrytty ominaisuuteen, jossa on tiliryhmävalinta.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Työnkulku |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme lopettavamme Kiinalaisten tositetyyppimäärityksen tukemisen ilman tiliryhmävalintaa 1.12.2020 mennessä. Lisätietoja uudesta suunnitelmasta on kohdassa [Uutta versiossa 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
