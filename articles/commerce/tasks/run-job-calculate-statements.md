---
title: Määritä ja suorita työ laskelmien laskemiseksi
description: Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412004"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>Määritä ja suorita työ laskelmien laskemiseksi

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten toistuvat erätyöt määritetään ja suoritetaan, kun valitulle myymälälle tai myymäläryhmälle luodaan ja lasketaan laskelmat. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.
2. Valitse Laske laskelmat.
    * Valitse tietty myymälä tai solmu, jos haluat luoda myymäläryhmälle erätyön.  
    * Lisää valinta nuolen avulla.  
3. Valitse Laajenna Suorita taustalla -välilehti.
4. Valitse Eräkäsittely-kohdassa Kyllä.
5. Valitse Toistuminen.
6. Syötä päivämäärä Aloituspäivä-kenttään.
7. Syötä Aloitusaika-kenttään aika.
8. Valitse päättymispäivämääräasetuksen arvoksi Ei.
9. Syötä PatternUnit-kenttään Päivät.
10. Syötä numero Per-kenttään.
11. Valitse OK.
12. Valitse OK.

