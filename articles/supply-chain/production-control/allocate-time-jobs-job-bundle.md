---
title: Ajan kohdistaminen työnipun töihin
description: Voit niputtaa töitä tuotannonohjauksessa. Tämän jälkeen voit käynnistää samanaikaisesti useita töitä luettelosivulta.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgBundleSlize, JmgProdParameters, JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 55591
ms.assetid: 358efce7-73c8-4d2a-a7f7-cb99b88ab6ee
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec07913e217cb3e33d5b58623643f02593c1eeae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426810"
---
# <a name="allocate-time-to-jobs-in-a-job-bundle"></a>Ajan kohdistaminen työnipun töihin

[!include [banner](../includes/banner.md)]

Voit niputtaa töitä tuotannonohjauksessa. Tämän jälkeen voit käynnistää samanaikaisesti useita töitä luettelosivulta.

Jos niputat töitä, sinun on määritettävä, miten kaikille töille rekisteröity kokonaisaika kohdistetaan yksittäisiin töihin. Voit määrittää kohdistuksen valitsemalla jonkin seuraavista asetuksista **Nipputyyppi**-kenttään **Kohdistustunnukset**-sivulla:

-   **Arvio** - Aika jaetaan töiden välillä töiden arvioidun ajan perusteella.
-   **Työt** – Aika jaetaan sen mukaan, kuinka monta työtä yhteensä on niputettu ja kuinka paljon aikaa on kulunut kaikkien töiden valmiiksi saamiseen.
-   **Nettoaika** – Aika jaetaan tasan samaan aikaan nipussa olevien töiden kesken.
-   **Reaaliaikainen** – Todellinen työaika kohdistetaan. Kustannukset voidaan laskea todellisten palkkakustannusten perusteella. **Huomautus:** **Reaaliaikainen**-kohdistustunnus on käytettävissä vain, jos yrityksessä käytetään työajan seurannan palkanlaskentatoimintoja.

Erilaisten kohdistustunnusten tuloksia voidaan selvittää seuraavalla esimerkillä.

## <a name="example-scenario"></a>Esimerkkiskenaario
Työjonossa on kolme työtä, jotka on saatava valmiiksi. Aloitat ensimmäisen työn, ja kun tämä työ on käynnissä, aloitat sekä toisen että kolmannen työn. Nämä kolme työtä ovat siis työnippu. Seuraavassa taulukossa näytetään kunkin työn arvioitu tuotantoaika.

| Työ   | Tuotantoaika |
|-------|-----------------|
| Työ 1 | 1 tunti          |
| Työ 2 | 3 tuntia         |
| Työ 3 | 4 tuntia         |
| Yhteensä | 8 tuntia         |

Seuraavassa taulukossa näkyvät tiettyyn työhön kuluneet, toteutuneet työtunnit.

| Työ    | Aloitusaika | Päättymisaika | Nipun aika |
|--------|------------|----------|-------------|
| Työ 1  | 09:00      | 11:00    | 2 tuntia     |
| Työ 2  | 10:00      | 13:00    | 3 tuntia     |
| Työ 3  | 10:00      | 15:00    | 5 tuntia     |
| Nippu | 09:00      | 15:00    | 6 tuntia     |

Seuraavissa osissa esitetään kunkin kohdistustunnuksen lasketun ajan tulokset.

## <a name="estimation-allocation-key"></a>Arvio-kohdistusavain
Seuraavassa taulukossa esitetään kaava, jolla kohdistettu aika lasketaan. Kaava on seuraava: Työkohtainen aika = nipun kokonaisaika × (työn arvioitu aika ÷ arvioitu kokonaisaika)

| Työ   | Resepti           | Kohdistettu aika |
|-------|-------------------|----------------|
| Työ 1 | 6 × (1 ÷ 8) tuntia | 0,75 tuntia      |
| Työ 2 | 6 × (3 ÷ 8) tuntia | 2,25 tuntia     |
| Työ 3 | 6 × (4 ÷ 8) tuntia | 3,00 tuntia     |

## <a name="jobs-allocation-key"></a>Työt-kohdistusavain
Seuraavassa taulukossa esitetään kaava, jolla kohdistettu aika lasketaan. Kaava on seuraava: Työkohtainen aika = nipun kokonaisaika ÷ töiden määrä

| Työ   | Resepti | Kohdistettu aika |
|-------|---------|----------------|
| Työ 1 | 6 ÷ 3   | 2 tuntia        |
| Työ 2 | 6 ÷ 3   | 2 tuntia        |
| Työ 3 | 6 ÷ 3   | 2 tuntia        |

## <a name="net-time-allocation-key"></a>Nettoaika-kohdistusavain
Seuraavassa taulukossa esitetään kaava, jolla kohdistettu aika lasketaan. Kaava on seuraava: Laskettu raporttikohtainen aika = nipun aika ÷ töiden määrä

|                              | 09:00–10:00 (1 tunti) | 10:00–11:00 (1 tunti) | 11:00–13:00 (2 tuntia) | 13:00–15:00 (2 tuntia) | Kohdistettu aika |
|------------------------------|----------------------|----------------------|-----------------------|-----------------------|----------------|
| Nipun työmäärä | 1                    | 3                    | 2                     | 1                     | Ei käytettävissä |
| Työ 1                        | 1 ÷ 1 = 1 tunti       | 1 ÷ 3 = 0.33 tuntia    | Ei käytettävissä        | Ei käytettävissä        | 1,33 tuntia     |
| Työ 2                        | Ei käytettävissä       | 1 ÷ 3 = 0.33 tuntia    | 2 ÷ 2 = 1 tunti        | Ei käytettävissä        | 1,33 tuntia     |
| Työ 3                        | Ei käytettävissä       | 1 ÷ 3 = 0.33 tuntia    | 2 ÷ 2 = 1 tunti        | 2 ÷ 1 = 2 tuntia       | 3,33 tuntia     |

## <a name="real-time-allocation-key"></a>Reaaliaikainen-kohdistusavain
Jos haluat, että tuotantokustannukset lasketaan todellisista kustannuksista, poista **Kustannusluokka**-asetus **Tuotantotilauksen oletusarvot** -sivulta. Seuraavassa taulukossa esitetään kaava, jolla kohdistettu aika lasketaan. Kaava on seuraava: Todellinen työkohtainen aika = todellinen aika nipussa

| Työ   | Toteutunut aika |
|-------|-------------|
| Työ 1 | 2 tuntia     |
| Työ 2 | 3 tuntia     |
| Työ 3 | 5 tuntia     |

Kyseessä on kolme työtä, joiden suorittajan tuntipalkka on 12,00 Yhdysvaltain dollaria. Työntekijä ei ansainnut töihin käyttämästään ajasta ylityöbonusta tai -lisää. Työntekijä on työskennellyt näiden kolmen niputetun työn parissa yhteensä 6 tuntia. Palkkakustannus on siis 6 × 12,00 USD = 72,00 USD. Kun käytät reaaliaikaista kohdistusta, tuntikohtainen kustannus lasketaan uudelleen Nettoaika-kaavan kertoimella. Tämän jälkeen kuhunkin työhön kulutettu todellinen aika siirretään käyttäen korjattua tuntikohtaista kustannushintaa. Esimerkissä käytetään vain kuusi tuntia, vaikka kohdistettu aika oli 10 tuntia. Seuraavassa taulukossa esitetään kaava, jolla kustannus lasketaan. Kaava on seuraava: Tuntikohtainen kustannus = (nipun työkohtainen kokonaisaika (nettoaika) ÷ todellinen työkohtainen aika) × tuntikohtainen peruskustannushinta

| Työ   | Korjatun tuntikohtaisen kustannuksen laskenta | Korjattu tuntikohtainen kustannus | Kohdistettu aika | Työn kokonaiskustannukset |
|-------|----------------------------------------|-------------------------|----------------|-------------------|
| Työ 1 | (1,33 ÷ 2) × 12,00 USD                 | 8,00 USD                | 2 tuntia        | 16,00 USD         |
| Työ 2 | (1,33 ÷ 3) × 12,00 USD                 | 5,33 USD                | 3 tuntia        | 16,00 USD         |
| Työ 3 | (3,33 ÷ 5) × 12,00 USD                 | 8,00 USD                | 5 tuntia        | 40,00 USD         |

Korjattu tuntikohtainen kustannus ja työn aika kirjataan tuotantokirjauskansioon. **Huomautus:** Valitsemalla **Kustannusluokka**-asetuksen **Tuotantotilauksen oletusarvot** -sivun **Yleinen**-välilehdellä, kunkin työn toteutunut aika siirretään tuotantokirjauskansioon, jossa kustannukset kohdistetaan kyseisen työn kustannusluokkaan.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]