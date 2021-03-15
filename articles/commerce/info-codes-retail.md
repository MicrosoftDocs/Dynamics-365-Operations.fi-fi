---
title: Tietokoodit ja tietokoodiryhmät
description: Tässä artikkelissa on yleistietoja tietokoodeista ja tietokoodiryhmistä sekä niiden käyttämisestä.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e9f84e3ffc79920fc6ef49a6391f76acdd89252a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012466"
---
# <a name="info-codes-and-info-code-groups"></a>Tietokoodit ja tietokoodiryhmät

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleistietoja tietokoodeista ja tietokoodiryhmistä sekä niiden käyttämisestä.

Tietokoodit tarjoavat tavan kerätä tietoja myyntipisteen rekisteriin. Voit käyttää tietokoodeja pyytämään kassanhoitajaa kirjoittamaan tiedot erilaisten myyntipisteen toimintojen aikana, kuten nimikkeen myynti, nimikkeen palautus tai asiakkaiden valinta. Kassat voivat valita syötteen luettelosta tai antaa sen koodina, numerona, päivämääränä tai tekstinä. Voit liittää tietokoodit ennalta määritettyihin myymälän toimiin, maksutapoihin, asiakkaisiin tai tiettyihin myyntipisteen tehtäviin. Voit käyttää tietokoodeja seuraavasti:

- Kerää lisätietoja tapahtuman aikana, kuten lennon numeron ja palautuksen syy.
- Kehote kassalle valita tiettyjen tuotteiden hintaluettelosta.
- Linkitä alikoodi tietokoodiin, joka kehottaa kassaa syöttämään tiedon tietyn tehtävän suorituksen aikana. Esimerkiksi kun asiakas palauttaa tuotteen, voit pyytää kassanhoitajaa kysymään tuotepalautuksen syy. Tämän jälkeen voit käyttää alikoodeja syyluettelon näyttämiseen, josta kassanhoitaja voi valita.
- Myy tuote tavallisessa myynnissä, alennetussa myynnissä tai ilmaisena tuotteena.
- Kehota kassanhoitajaa kirjoittamaan arvo tai valitsemaan tarvittava arvo alikoodiluettelosta kassaa avattaessa ilman myynnin työvaiheen suorittamista.

## <a name="info-codes-group"></a>Tietokoodiryhmä

Voit luoda tietokoodiryhmiä Kaupassa. Tietokoodiryhmät lisäävät joustavuutta ja antavat mahdollisuuden määrittää vähemmän tietokoodeja ja käyttää niitä monipuolisemmin. Voit käyttää tietokoodiryhmiä seuraavilla tavoilla:

- Määritä vähemmän tietokoodeja ja käytä niitä helposti uudelleen. Tietokoodiryhmissä olevilla tietokoodeilla ei ole ennalta määritettyjä riippuvuuksia muissa tietokoodeissa. Voit sisällyttää samat kooditiedot useisiin tietokoodiryhmiin ja sitten käyttää priorisointia esittämään samat tietokoodit siinä järjestyksessä, joka vastaa kulloisiakin vaatimuksia.
- Linkitä tietokoodit muihin tietokoodeihin tai tietokoodiryhmiin, jotta voit kerätä tietoja tuotteesta tai tapahtumasta määrittämättä erillistä tietokoodia tai linkitettyä tietokoodia jokaiselle skenaariolle.

## <a name="info-code-examples"></a>Tietokoodiesimerkkejä

**Esimerkki 1: Käytä tietokoodit uudelleen**

Voit linkittää tietokoodit siten, että kun tietokoodi käynnistyy, toinen koodi käynnistyy heti sen jälkeen. Kun esimerkiksi myyt tiettyjä tuotteita, kehota kassanhoitaja kysymään asiakkailta, haluavatko he ostaa paristoja ja tuotetakuun. Muiden tuotteiden kohdalla voit kehottaa kassanhoitajaa kysymään asiakkaalta, haluaako tämä ostaa paristoja, ja pyytämään asiakkaan postinumeron. Jos näissä tilanteissa luodaan linkitettyjä tietokoodeja, sinun on määritettävä tietokoodin jokainen muutos siten, että kassanhoitajaa kehotetaan pyytämään oikeat tiedot. Jos käytät tietokoodiryhmiä, yleiset tietokoodit, kuten paristojen pyytäminen, voidaan määrittää kerran ja sitten käyttää uudelleen useissa tietokoodiryhmissä. Voit käyttää myös priorisointia tietokoodiryhmissä määrittämään järjestyksen, jossa kehotteita näytetään.

**Esimerkki 2: Linkitä tietokoodit tietokoodiryhmiin**

Kun myyt tiettyjä tuotteita, esimerkiksi kannettavat laitteet, haluat aina kerätä tietyt tiedot, kuten puhelinnumero, kannettavat laitteet tunnus (MEID) ja sarjanumero. Kuitenkin haluat myös kerätä eri tietoja taulutietokonesovellukseen kuin matkapuhelimeen. Voit määrittää tietokoodiryhmän, joka sisältää kehotteen puhelinnumeron, tunnuksen ja sarjanumeron kysymisestä ja linkittää sitten tietokoodiryhmän yksittäiseen tietokoodiin. Kun tuotetta koskeva infokoodi toteutuu, tietokoodiryhmä voidaan määrittää käynnistymään seuraavaksi, jotta voit kerätä yleisiä tietoja tarvitsematta määrittää useita linkitettyjä infokoodisarjoja kullekin laitteelle.


[!INCLUDE[footer-include](../includes/footer-banner.md)]