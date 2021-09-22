---
title: Varastokirjauskansio on lukittu eikä työnkulun erätyö toimi
description: Jokin toiminto on lukinnut varastokirjauskansion eikä sitä vapauteta
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
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476201"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Varastokirjauskansio on lukittu eikä työnkulun erätyö toimi

## <a name="symptoms"></a>Oireet

Jokin toiminto on lukinnut varastokirjauskansion eikä sitä vapauteta. Jos esimerkiksi tuntematon virhe esiintyy kirjauksen aikana (sillä kirjaus on järjestelmän lukitustoiminto), kirjauskansio voi jäädä järjestelmän lukitsemaan tilaan. Siinä tapauksessa työnkulun työnimikkeen käsittelijä ilmoittaa virheen, kun se tarkistaa lukituksen.

## <a name="resolution"></a>Ratkaisu

Kirjaudu Supply Chain Managementin SQL Server -esiintymään ja tarkista, onko **InventJournalTable.SystemBlocked**-asetuksena *1*. Jos näin on, varmista, ettei kirjauskansio ole lukitussa tilassa ja nollaa sitten **InventJournalTable.SystemBlocked**-asetukseksi *0*.
