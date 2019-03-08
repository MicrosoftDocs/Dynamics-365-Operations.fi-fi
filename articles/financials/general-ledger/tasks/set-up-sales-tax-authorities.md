---
title: Arvonlisäveroviranomaisten määrittäminen
description: Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 909433a04c1185039938f6233b30c235e7b8ed8b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "366348"
---
# <a name="set-up-sales-tax-authorities"></a>Arvonlisäveroviranomaisten määrittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Arvonlisäveroviranomaiset ovat yksiköitä, joille on raportoitava kerättävästä arvonlisäverosta ja joille arvonlisävero maksetaan. Yritys voi maksaa arvonlisäverot suoraan viranomaiselle tai arvonlisäveroviranomaiselle luodun toimittajatilin kautta. Jos valitset tämän vaihtoehdon, yritys voi maksaa arvonlisäveroviranomaiselle ajoissa tavanomaista maksurutiinia käyttäen. Jos veroviranomaista ei määritetä toimittajaksi, jonkun on laadittava maksut veroviranomaiselle manuaalisesti asianmukaisena eräpäivänä. Tässä tehtävässä käytetään esittely-yritystä USMF.

1. Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroviranomaiset.
2. Valitse Uusi.
3. Kirjoita arvo Viranomainen-kenttään.
4. Kirjoita arvo Nimi-kenttään.
5. Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse maasi/alueesi raportin asettelu, jos sellainen on valittavissa. Jos raportin asettelut eivät vastaa arvonlisäveroviranomaisen vaatimuksia, käytä oletusasettelua.
9. Määritä, miten veron maksettava kokonaissumma on pyöristettävä, syöttämällä arvo Pyöristystapa- ja Pyöristys-kenttään. Pyöristyserot kirjataan tileille kirjanpidolle määritettyjä automaattisia tapahtumia varten.
10. Syötä Pyöristys-kenttään numero.
11. Valitse Tallenna.

