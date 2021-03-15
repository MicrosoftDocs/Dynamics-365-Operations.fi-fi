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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4847b5f3f50cc74c5b4854e1f0daedd64785baf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994562"
---
# <a name="set-up-sales-tax-authorities"></a>Arvonlisäveroviranomaisten määrittäminen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]