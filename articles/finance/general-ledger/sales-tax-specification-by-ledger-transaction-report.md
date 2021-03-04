---
title: Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raportti
description: Tässä aiheessa selitetään, kuinka Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raporttia voidaan käyttää sellaisten kirjanpitotapahtumien tietojen tarkastelemiseen ja tulostamiseen, joille on laskettu arvonlisävero.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442620"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Arvonlisäveron erittely kirjanpitotapahtuman mukaan -raportti
[!include [banner](../includes/banner.md)]

Tässä aiheessa selitetään, kuinka **Arvonlisäveron erittely kirjanpitotapahtuman mukaan** -raporttia voidaan käyttää sellaisten kirjanpitotapahtumien tietojen tarkastelemiseen ja tulostamiseen, joille on laskettu arvonlisävero.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Verotilit vs. muut kuin verotilit

**Arvonlisäveron erittely kirjanpitotapahtuman mukaan** -raportti näyttää sekä verotilien että muiden kuin verotilien verotapahtumat. Nämä tilit on luokiteltu seuraavalla tavalla:

- **Verotili** – Tiliä pidetään verotilinä, kun verotapahtuma kirjataan ja **Arvonlisävero**-kirjauskansiorivin päätili on verotili, kuten maksettavan arvonlisäveron tili tai saatava arvonlisäveron tili.
- **Muu kuin verotili** –Tiliä pidetään muuna kuin verotilinä, kun verotapahtuma kirjataan ja alkuperäisen tapahtuman päätili on muu kuin verotili, kuten tuottotili tai kulutili.

Verotilien **Alkuperä**-, **Saatava arvonlisävero**- ja **Maksettava arvonlisävero** -sarakkeissa näytetään **0** (nolla). Muissa kuin verotileissä näissä sarakkeissa näytetään summat.

## <a name="filtering-the-data-on-the-report"></a>Raportin tietojen suodattaminen

Kun luot raportin, seuraavat oletuskentät ovat käytettävissä. Voit käyttää näitä kenttiä suodattaaksesi raportissa näytettäviä tietoa.

| Kenttä                      | Kuvaus |
|----------------------------|-------------|
| Päivämäärä                       | Määritä verotapahtumien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä. |
| Päätili               | Määritä päätilien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä. |
| Arvonlisäverokoodi             | Määritä arvonlisäverokoodien ajanjakso käyttämällä **Alkamispäivä**- ja **Päättymispäivä**-osioiden kenttiä. |
| Ryhmittely                   | Valitse, ryhmitetäänkö raportti kirjanpitotilin vai arvonlisäverokoodin mukaan. |
| Välisumma arvonlisäverokoodeittain | Määritä täksi asetukseksi **Kyllä**, jos haluat näyttää välisummat arvonlisäverokoodin mukaan. |
| Vain kokonaissummat                | Määritä täksi asetukseksi **Kyllä**, jos haluat näyttää vain kokonaissummat. |
| Vain päätilit         | Valitse täksi asetukseksi **Kyllä**, jos haluat sisällyttää raporttiin vain päätilit. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Vain muiden kuin verotilien näyttäminen raportissa

Jos haluat näyttää raportissa vain muut kuin verotilit, määritä suodatusehto, kuten tähtimerkki (\*), seuraavan kuvan osoittamalla tavalla.

![Raportti, joka näyttää muut kuin verotilit](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]