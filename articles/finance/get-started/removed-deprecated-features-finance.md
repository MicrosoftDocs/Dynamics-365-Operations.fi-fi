---
title: Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet
description: Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.
author: kfend
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 070c61df14db4d2538b129b01defd4b82db0b8a7
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462298"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on lisätietoja talous- ja toimintosovellusten objekteista: [Tekniset viitetiedot](/dynamics/s-e/global/axtechrefrep_61). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin talous- ja toimintosovellusten versiossa.

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Financen version 10.0.30 poistetut tai vanhentuneet ominaisuudet

### <a name="revenue-recognition"></a>Tuottokirjaus

[Tuottokirjaus](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Poiston tai vanhentumisen syy** |Korvattu parannetulla ominaisuudella, joka on [tilauslaskutus](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan** | Hakemus |
| **Käytön asetukset** | Kaikki |
| **Tila** | Vanhentunut: Huhtikuun 2023 jälkeen tuoton kirjauksen toiminto Dynamics 365 Financessa ei enää vastaanota tukea ohjelmakorjauksien muodossa. Pyydämme asiakkaita käyttämään parannettua ominaisuutta, joka on [tilauslaskutus](../../finance/accounts-receivable/subscription-billing-summary.md). Lokakuussa 2023 tuottojen tunnistustoiminto ei ole enää käytettävissä. Pyydämme asiakkaita siirtymään parannetun tilauslaskutustoiminnon käyttäjiksi. Tuottokirjauksen osana olevalle nipputoiminnolle ei ole suunniteltu korvaustoimintoa tällä hetkellä.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Financen version 10.0.29 poistetut tai vanhentuneet ominaisuudet

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Varastosiirtotilaukset, joiden siirron hintaan sisältyy vero

[Varastosiirtotilaukset, joiden siirron hintaan sisältyy vero](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Poiston tai vanhentumisen syy** | Korvattu parannetulla [Intian varastosiirtotilaukset](../../finance/localizations/apac-ind-stock-transfer.md) -ominaisuudella|
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan** | Hakemus |
| **Käytön asetukset** | Kaikki |
| **Tila** | Vanhentunut: **Varastosiirtotilaukset, joiden siirron hintaan sisältyy vero** -ominaisuutta ei enää tueta huhtikuun 2023 jälkeen, eli sille ei tarjota enää virheiden korjauksia tai tietoturvakorjauksia. Pyydämme asiakkaita käyttämään parannettua [Intian varastosiirtotilaukset](../../finance/localizations/apac-ind-stock-transfer.md) -ominaisuutta. **Varastosiirtotilaukset, joiden siirron hintaan sisältyy vero** -ominaisuus ei ole enää käytettävissä lokakuun 2023 jälkeen, ja asiakkaita pyydetään käyttämään parannettua ominaisuutta. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Tiliotteen tuonti ja vienti Positive pay -tiedostolle

| &nbsp;  | &nbsp;  |
|---|---|
| **Poiston tai vanhentumisen syy** |Korvattu parannetulla toiminnolla – tiliotteiden tuonti ja Positive Pay -tiedostojen vienti.| 
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: XSLT-toiminnot tiedostojen tuonnissa ja viennissä ei enää tueta ohjelma- ja suojauskorjauksia. Asiakkaita pyydetään käyttämään parannettua toimintoa: [Positive Pay -tiedostojen määrittäminen sähköisen raportoinnin avulla](../../finance/accounts-payable/set-up-positive-pay-er.md) ja [Pankkitilin täsmäytyksen tuonnin lisätoimintojen määrittäminen sähköisen raportoinnin avulla](../../finance/accounts-payable/import-bai2-er.md). Vuoden 2022 syyskuun jälkeen XSLT-toiminnot eivät ole enää käytettävissä. Asiakkaita pyydetään siirtymään parannettujen toimintojen käyttäjiksi.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Financen version 10.0.26 poistetut tai vanhentuneet ominaisuudet

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Suomen arvonlisäveroraportti (suunnittelu raportointikoodien perusteella)

[Suomen arvonlisäveroraportti](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella ALV-ilmoituksen mallilla, [Suomen ALV-ilmoituksella](../localizations/emea-fin-vat-declaration.md) |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suomen arvonlisäveroraporttia ei enää tueta maaliskuun 1. päivän 2023 jälkeen (Suomen raportin asettelu). Uudet **ALV-ilmoitus XML (FI**) ja **ALV-ilmoitus Excel (FI)** Sähköiset raportointimuodot (ER) otetaan käyttöön mallin **Veroilmoitus** mallissa. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Financen version 10.0.24 poistetut tai vanhentuneet ominaisuudet

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Ruotsin arvonlisäveroraportti (suunnittelu raportointikoodien perusteella)

[Ruotsin arvonlisäveroraportti](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella ALV-ilmoituksen mallilla, [Ruotsin ALV-ilmoituksella](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Ruotsin arvonlisäveroraporttia ei enää tueta joulukuun 1. päivän 2022 jälkeen (Ruotsin raportin asettelu). Uudet **ALV-ilmoitus XML (SE**) ja **ALV-ilmoitus Excel (SE)** Sähköiset raportointimuodot (ER) otetaan käyttöön mallin **Veroilmoitus** mallissa. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Itävallan ALV-ilmoitus (suunnittelu raportointikoodien perusteella)

[ALV-ilmoituksen erittely, Itävalta](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella ALV-ilmoituksen mallilla, [Itävallan ALV-ilmoituksella](../localizations/emea-aut-vat-declaration-austria.md) |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme 1.12.2022 mennessä, ettei **ALV-ilmoitusta (AT)** sähköisessä raportoinnissa (ER) **ALV-ilmoitusmallin (AT)** alla enää tueta. Uudet **ALV-ilmoitus XML (AT)** ja **ALV-ilmoitus Excel (AT)** otetaan käyttöön mallin **Veroilmoitus**-mallissa. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>Saksan ELSTER-ilmoitus (suunnittelu raportointikoodien perusteella)

[ALV-ilmoitus](../localizations/emea-de-vat-declaration.md)</br>
[Sähköisen veroilmoituksen määrittäminen, Saksa](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[ALV-ilmoituksen antaminen sähköisesti (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella ALV-ilmoituksen mallilla, [Saksan ALV-ilmoituksella](../localizations/emea-deu-vat-declaration-germany.md) |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme 1.12.2022 mennessä, ettei **Elster (DE)**- ja **Elster-malli (DE)**- sähköisen raportoinnin (ER) -muotoja enää tueta. Uudet **ALV-ilmoitus XML (DE)** ja **ALV-ilmoitus Excel (DE)** otetaan käyttöön mallin **Veroilmoitus**-mallissa. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>Alankomaiden OB-ilmoitus (suunnittelu raportointikoodien perusteella)

[OB-ilmoitus](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella ALV-ilmoituksen mallilla, [Alankomaiden ALV-ilmoituksella](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme 1.12.2022 mennessä lopettavamme **OB-ilmoituksen (NL)** ja **OB-ilmoitusmallin** sähköisen raportoinnin (ER) tukemisen. Uudet **ALV-ilmoitus XML (NL)** ja **ALV-ilmoitus Excel (NL)** otetaan käyttöön mallin **Veroilmoitus**-mallissa. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Financen version 10.0.20 poistetut tai vanhentuneet ominaisuudet

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>"RTIR Query Invoice Data Request (HU)" Sähköisen raportoinnin (ER) muodon konfigurointi

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ei sisälly sähköisten viestien käsittelyyn sähköisten viestien välitysjärjestelmän kanssa |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Huhtikuun 15.4.2022 mennessä suunnitelma ei enää tue MUODON RTIR Query Invoice Data Request (HU) -muotoa. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"Ranskan FEC-auditointitiedosto" Sähköisen raportoinnin (ER) muoto Ranskalle "Saksan tarkistustiedostotuloste" -muodon alaisena

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan uudella "FEC-auditointitiedosto (FR)" -muodolla |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1.5.2022 mennessä ei enää tueta kohdetta "Ranskan FEC-auditointitiedosto" Sähköisen raportoinnin (ER) muoto Ranskalle "Saksan tarkistustiedostotuloste" -muodon alaisena. Tietojen vientimalli -kohdassa käytetään sen sijaan uutta FEC-auditointitiedostomuotoa (FR). |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Financen version 10.0.17 poistetut tai vanhentuneet ominaisuudet

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-tietovarasto sähköisen raportoinnin konfiguraatioiden tallennusvaihtoehtona

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvataan Regulatory Configuration Service (RCS) -yleistietovarastolla. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Dynamics 365 Finance-, Supply Chain Management- ja Project Operations -tuotteet|
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme että Microsoft Dynamics Lifecycle Services (LCS) -tietovarastoa ei enää tueta 1.4.2022 alkaen sähköisen raportoinnin (ER) konfiguraatioiden tallennussäilönä. Uudet Microsoftin ER-konfiguraatiot julkaistaan yksinomaan yleisestä tietovarastosta ladattavaksi. Yleinen tietovarasto on käytettävissä Dynamics 365 -tuotteiden ja RCS:n kautta. Lisätietoja on kohdassa [ER-konfiguraatioiden tuominen RCS:stä](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) ja [Regulatory Configuration Service – Lifecycle Services -tallennustilan vanhentuminen](../localizations/rcs-lcs-repo-dep-faq.md). |

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

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Ei vanhentunut: Puolan SSRS-raportit, maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri - toimintojen viite PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ei lakisääteistä edellytystä.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä (Excel-muoto vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa - JPK_VDEK) |
| **Tuotealueet, joihin vaikutetaan**         | Hakemus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Ei vanhentunut: 27.4.2021 alkaen tuemme SSRS-raportteja: **Maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri – toimintojen viite PL-00014**. Excel-muodon esimerkki vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa (JPK_VDEK) on myös otettu käyttöön. |

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

