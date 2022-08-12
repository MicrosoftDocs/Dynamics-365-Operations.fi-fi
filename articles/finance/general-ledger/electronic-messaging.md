---
title: Sähköiset sanomat
description: Tämä artikkeli sisältää Microsoft Dynamics 365 Financen sähköisten sanomien yleiskatsauksen ja määritystiedot.
author: liza-golub
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4e765c6d56e0ab6d209c27a70fd4b7e52273c103
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069877"
---
# <a name="electronic-messaging"></a>Sähköiset sanomat

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää **Sähköiset sanomat** (EM) -ominaisuuden yleiskatsauksen ja määritystiedot.

Useiden eri maiden ja eri alueiden hallitukset ja viranomaiset eri puolilla maailmaa ovat äskettäin ottaneet käyttöön raportointivaatimuksia, jotka kyseisissä maissa ja kyseisillä alueilla rekisteröityneitä yrityksiä. Vaatimusten tarkoituksena on mahdollistaa tietojen saaminen kyseisistä yrityksistä sähköisessä muodossa suoraan niistä järjestelmistä, joissa tiedot kirjattiin, tallennettiin ja käsiteltiin.

Microsoft Dynamics 365 Financen EM-ominaisuus tukee erilaisia sähköisiä prosesseja Financen sekä sellaisten julkishallinnon ja viranomaisten järjestelmien välillä, jotka mahdollistavat virallisten tietojen raportoinnin, lähettämisen ja vastaanottamisen.

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

## <a name="security-privileges"></a>Suojausoikeudet

Seuraavat suojausoikeudet ovat käytettävissä sähköisiä sanomia varten.

| Suojausoikeus           | Käyttöoikeustaso | Liitos |
|------------------------------|--------------|-------------|
| Säilytä sähköiset sanomat | Tämä oikeus antaa täyden pääsyn EM-ominaisuuksiin. Jos sinulla on tämä oikeus, voit määrittää sähköisen viestinnän ja suorittaa kaiken käsittelyn. | Tämä oikeus sisältyy **Ylläpidä myyntiverotapahtumia** -käyttöoikeusvelvollisuuteen. Kyseinen velvollisuus vuorostaan sisältyy **Kirjanpitäjä**-käyttöoikeusrooliin. |
| Näytä sähköiset sanomat     | Tämä oikeus antaa vain luku -pääsyn EM-ominaisuuksiin. Jos sinulla on tämä oikeus, voit tarkastella sähköisen viestinnän asetuksia ja sanomia. Et kuitenkaan voi määrittää tai suorittaa mitään. | Tämä oikeus sisältyy **Tarkastele myyntiveron tapahtumatilaa** -käyttöoikeusvelvollisuuteen. Kyseinen velvollisuus vuorostaan sisältyy seuraaviin käyttöoikeusrooleihin:<ul><li>Perintäjohtaja</li><li>Myyntireskontranhoitaja</li><li>Myyntireskontrapäällikkö</li><li>Verokirjanpitäjä</li><li>Kirjanpitäjä</li><li>Laskentapäällikkö</li><li>Taloushallintopäällikkö</li><li>Myyntipäällikkö</li><li>Ostoreskontra-assistentti</li></ul> |
| Käytä sähköisiä viestejä  | Tämä oikeus antaa käyttöoikeuden vain **Sähköiset sanomat**- ja **Sähköisen sanoman kohteet** -sivuihin. Jos sinulla on tämä oikeus, voit suorittaa kaiken käsittelyn, joka kutsutaan kyseiseltä sivuilta. | Tämä oikeus sisältyy **Käytä sähköisiä sanomia** -käyttöoikeusvelvollisuuteen. Kyseinen velvollisuus vuorostaan sisältyy **Sähköisten sanomien käyttäjä** -käyttöoikeusrooliin. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM-ominaisuuden tukemat maakohtaisiin säännöksiin perustuvat ominaisuudet

Seuraavassa taulukossa on tietoja joistakin maakohtaisiin säännöksiin perustuvista ominaisuuksista, joita EM-ominaisuus tukee.

| Maa tai alue     | Toiminnon nimi | Ominaisuuden esittelyn tallennus |
|-------------|--------------|------------------------|
| Espanja       | [ALV-tietojen välitön lähetys (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Unkari     | [Verkkolaskutusjärjestelmä](../localizations/emea-hun-online-invoicing.md) | |
| Yhdistynyt kuningaskunta | [Making Tax Digital (MTD) – ALV-ilmoituksen lähetys](../localizations/emea-gbr-mtd-vat-integration.md) | [Talous- ja toimintosovellukset: UK Digital Tax - ALV-ilmoitus Dynamics 365:ssä](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
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
| Norja      | [ALV-palautus ja suora Altinnille lähetys](../localizations/emea-nor-vat-return.md) | [Uusi ALV-palautus ja suora lähetys Altinnille Dynamics 365 Financessa](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Ranska      | [ALV-ilmoitus (Ranska)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Itävalta     | [ALV-ilmoitus (Itävalta)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Saksa     | [ALV-ilmoitus (Saksa)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Alankomaat | [Alankomaiden ALV-ilmoitus](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Ruotsi      | [ALV-ilmoitus (Ruotsi)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Sveitsi | [ALV-ilmoitus (Sveitsi)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


