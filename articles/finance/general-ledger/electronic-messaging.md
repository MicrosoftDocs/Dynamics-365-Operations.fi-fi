---
title: Sähköiset sanomat
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Financen sähköisten sanomien yleiskatsaus ja määritystiedot.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433716"
---
# <a name="electronic-messaging"></a>Sähköiset sanomat

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on **Sähköiset sanomat** (EM) -ominaisuuden yleiskatsaus ja määritystiedot.

Useiden eri maiden ja eri alueiden hallitukset ja viranomaiset eri puolilla maailmaa ovat äskettäin ottaneet käyttöön raportointivaatimuksia, jotka kyseisissä maissa ja kyseisillä alueilla rekisteröityneitä yrityksiä. Vaatimusten tarkoituksena on mahdollistaa tietojen saaminen kyseisistä yrityksistä sähköisessä muodossa suoraan niistä järjestelmistä, joissa tiedot kirjattiin, tallennettiin ja käsiteltiin.

Microsoft Dynamics 365 Finance EM-ominaisuus tukee erilaisia sähköisiä prosesseja Financen sekä sellaisten julkishallinnon ja viranomaisten järjestelmien välillä, jotka mahdollistavat virallisten tietojen raportoinnin, lähettämisen ja vastaanottamisen.

EM-ominaisuus on integroitu **Sähköinen raportointi** (ER) -moduuliin. Voit määrittää ER-muotoja sähköisiä sanomia varten. Lisätietoja on kohdassa [Sähköinen raportointi (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>EM-ominaisuus peruskäsitteet

EM-ominaisuus perustuu seuraaviin entiteetteihin:

- **Sähköinen sanoma** – Raportti tai ilmoitus, joka tulisi raportoida tai lähettää sisäisesti, kuten verotoimistoon lähetettävä raportti.
- **Sähköisen sanoman nimikkeet** – tietueet, joiden on sisällyttävä raportoitavaan sanomaan.
- **Sähköisen sanoman käsittely** – Toimintoketju, jonka avulla kerätään tarvittavat tiedot, luodaan raportit, tallennetaan tiedot Azure Blob -säilöön, lähetetään raportit järjestelmän ulkopuolelle, vastaanotetaan vastaukset järjestelmän ulkopuolelta ja päivitetään tietokanta vastaanotettujen tietojen perusteella. Ketjun toiminnat voivat olla linkitettyjä tai linkittämättömiä.

Seuraava kuva näyttää EM-ominaisuuden työnkulun.

![Sähköisten sanomien tietovuo.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM-ominaisuuden tukemat skenaariot

EM-ominaisuus tukee seuraavia skenaarioita:

- Luo manuaalisesti sanomia ja luo raportteja, jotka perustuvat erityyppisiin ER-vientimuotoihin. Näihin tyyppeihin sisältyvät Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, teksti ja Microsoft Word.
- Luo ja käsittele automaattisesti sanomia, jotka perustuvat viranomaiselta liitetyn ER-tuontimuodon avulla pyydettyihin ja vastaanotettuihin tietoihin.
- Tietojen kerääminen ja käsittely tietolähteestä sanoman nimikkeinä. Tietolähde on Finance-taulu.
- Lisätietojen tallentaminen ja eri arvojen arviointi kutsumalla erityisesti määritettyjä suorittavia luokkia suhteessa sanomiin tai sanoman nimikkeisiin.
- Sanoman nimikkeissä kerättyjen tietojen koostaminen, kyseisten tietojen jakaminen sanoman mukaan ja liitetyissä ER-vientimuodoissa olevien raporttien luominen.
- Lähetä luodut raportit verkkopalveluun käyttämällä Azure Key Vaultiin tallennettuja suojaustietoja.
- Vastauksen vastaanottaminen verkkopalvelusta, vastauksen tulkinta ja Financen tietojen päivittäminen tarvittaessa.
- Kaikkien luotujen raporttien tallentaminen ja tarkastelu.
- Kaikkien niiden lokitietojen tallentaminen ja tarkasteleminen, jotka liittyvät sanoman tai sanoman nimikkeen yhteydessä suoritettuihin toimintoihin.
- Käsittelyn hallinta sanoman ja sanoman nimikkeen erilaisten tilojen avulla.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM-ominaisuuden tukemat maakohtaisiin säännöksiin perustuvat ominaisuudet

Seuraavassa taulukossa on tietoja joistakin maakohtaisiin säännöksiin perustuvista ominaisuuksista, joita EM-ominaisuus tukee.

| Maa tai alue     | Toiminnon nimi | Ominaisuuden esittelyn tallennus |
|-------------|--------------|------------------------|
| Espanja       | [ALV-tietojen välitön lähetys (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Unkari     | [Verkkolaskutusjärjestelmä](../localizations/emea-hun-online-invoicing.md) | |
| Iso-Britannia | [Making Tax Digital (MTD) – ALV-ilmoituksen lähetys](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: UK Digital Tax - ALV-ilmoitus Dynamics 365:ssä](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Liettua   | [i.SAF-raportointi](../localizations/emea-ltu-isaf.md) | |
| Puola      | [ALV-ilmoitus ja rekisterit (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK:n ALV-auditointirekisterit](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Alankomaat | [Alankomaiden ALV-ilmoitus](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tšekin tasavalta | [ALV-ilmoitus](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilia      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Venäjä      | [ALV-ilmoitus](../localizations/rus-vat-declaration.md) | |
| Venäjä      | [Kirjanpidon raportoiminen sähköisessä muodossa](../localizations/rus-accounting-reporting.md) | |
| Venäjä      | [Voittojen veroilmoitus](../localizations/rus-profit-tax-declaration.md) | |
| Venäjä      | [Arvioitu veroilmoitus](../localizations/rus-assessed-tax-declaration.md) | |
| Venäjä      | [Kuljetusveroilmoitus](../localizations/rus-transport-tax-declaration.md) | |
| Venäjä      | [Kiinteistöveroilmoitus](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

