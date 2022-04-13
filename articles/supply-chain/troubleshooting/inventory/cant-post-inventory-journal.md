---
title: Varastokirjauskansion työnkulku ei koskaan valmistu eikä kirjauskansiota voi käsitellä
description: Kun kirjauskansion hyväksyntätyönkulku lähetetään, työnkulun käsittely lakkaa vastaamasta eikä kirjauskansioita voi muokata tai käsitellä.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488964"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Varastokirjauskansion työnkulku ei koskaan valmistu eikä kirjauskansiota voi käsitellä

## <a name="symptoms"></a>Oireet

Kun kirjauskansion hyväksyntätyönkulku lähetetään, työnkulun käsittely lakkaa vastaamasta eikä kirjauskansioita voi muokata tai käsitellä.

## <a name="resolution"></a>Ratkaisu

On useita syitä, miksi työnkulun käsittely ei ehkä valmistu. Tarkista seuraavat:

- Valitse **Varastonhallinta &gt; Asetukset &gt; Varastonhallinnan työkulut** ja tarkastele ongelmallisen työnkulun määritystä. Lisätietoja on kohdassa [Varastokirjauskansioin hyväksyntätyönkulut](../../inventory/inventory-journal-workflow.md).
- Työnkulussa voi esiintyä poikkeus tai virhe. Tarkastele ongelmallisen työnkulun työnimikehistoriaa ja katso, onko siinä työnkulun päättävää sovellusvirhettä.
- Varastokirjauskansio voidaan päivittää tai sitä voi muokata vain, jos se on hyväksytty. Jos peruutus on aktivoitu, voit yrittää peruuttaa kirjauskansion. Työnkulun erätyön suorittamisen keskeyttämiseen voi olla useita syitä. Työnkulkukehyksen ongelma voi aiheuttaa osan näistä syistä.
