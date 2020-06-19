---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b951c9074c68a9f7592c17e0688498880397b223
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406540"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1 – Tietomallin suunnittelu)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.


## <a name="create-a-new-data-model"></a>Luo uusi tietomalli
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, että Litware, Inc. -lähde on käytettävissä ja merkitty aktiiviseksi.  
2. Valitse Raportointikonfiguraatiot.
3. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
4. Syötä Nimi-kenttään "Taloushallinnon dimensioiden esimerkkimalli".
5. Valitse Luo konfiguraatio.
6. Valitse Suunnittelutoiminto.
7. Avaa valintaikkuna valitsemalla Uusi.
8. Kirjoita Nimi-kenttään "Kirjaus".
9. ValitseLisää.
10. Avaa valintaikkuna valitsemalla Uusi.
11. Syötä Nimi-kenttään Yritys.
12. ValitseLisää.
    * Malliin ei lisätä uutta tietueluetteloa. Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden asetukset (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille). Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension asetuksia.  
13. Avaa valintaikkuna valitsemalla Uusi.
14. Kirjoita Nimi-kenttään "Dimensioiden asetus".
15. Valitse Nimiketyyppi-kentässä Tietueluettelo.
16. ValitseLisää.
17. Avaa valintaikkuna valitsemalla Uusi.
18. Kirjoita Nimi-kenttään "Koodi".
19. Valitse Nimiketyyppi-kentässä Merkkijono.
20. ValitseLisää.
21. Avaa valintaikkuna valitsemalla Uusi.
22. Syötä Nimi-kenttään Nimi.
23. ValitseLisää.
24. Valitse puussa "Entry".
25. Avaa valintaikkuna valitsemalla Uusi.
26. Kirjoita Nimi-kenttään "Kirjauskansio".
27. Valitse Nimiketyyppi-kentässä Tietueluettelo.
28. ValitseLisää.
29. Avaa valintaikkuna valitsemalla Uusi.
30. Kirjoita Nimi-kenttään "Erä".
31. Valitse Nimiketyyppi-kentässä Merkkijono.
32. ValitseLisää.
33. Avaa valintaikkuna valitsemalla Uusi.
34. Kirjoita Nimi-kenttään "Tapahtuma".
35. Valitse Nimiketyyppi-kentässä Tietueluettelo.
36. ValitseLisää.
37. Avaa valintaikkuna valitsemalla Uusi.
38. Kirjoita Nimi-kenttään "Päivämäärä".
39. Valitse Nimiketyyppi-kentässä Päivämäärä.
40. ValitseLisää.
41. Avaa valintaikkuna valitsemalla Uusi.
42. Kirjoita Nimi -kenttään "Veloitus".
43. Valitse Nimiketyyppi-kentässä Reaaliluku.
44. ValitseLisää.
45. Avaa valintaikkuna valitsemalla Uusi.
46. Syötä Nimi-kenttään "Hyvitys".
47. ValitseLisää.
48. Avaa valintaikkuna valitsemalla Uusi.
49. Syötä Nimi-kenttään Valuutta.
50. Valitse Nimiketyyppi-kentässä Merkkijono.
51. ValitseLisää.
52. Avaa valintaikkuna valitsemalla Uusi.
53. Kirjoita Nimi-kenttään "Tosite".
54. ValitseLisää.
55. Avaa valintaikkuna valitsemalla Uusi.
56. Kirjoita Nimi-kenttään "Dimensioiden tiedot".
57. Valitse Nimiketyyppi-kentässä Tietueluettelo.
58. ValitseLisää.
    * Malliin on lisätty uusi tietueluettelo. Tässä luettelossa näytetään valittujen taloushallinnon dimensioiden arvot (kaikille tätä mallia tietolähteenä käyttäville ER-raporteille). Jokainen taloushallinnon dimensio esitetään tässä luettelossa tietueena, jonka asianmukaiset kentät edustavat dimension arvoja. Dimension nimi esitetään myös tässä tietueessa käytettävänä kenttänä valintatoimintoa varten tarvittaessa.  
59. Avaa valintaikkuna valitsemalla Uusi.
60. Kirjoita Nimi-kenttään "Koodi".
61. Valitse Nimiketyyppi-kentässä Merkkijono.
62. ValitseLisää.
63. Avaa valintaikkuna valitsemalla Uusi.
64. Syötä Nimi-kenttään kuvaus.
65. ValitseLisää.
66. Avaa valintaikkuna valitsemalla Uusi.
67. Syötä Nimi-kenttään Nimi.
68. ValitseLisää.
69. Valitse Tallenna.
70. Sulje sivu.

![ER-tietomallin suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-data-model.png)

