---
title: "Tietokoodit ja tietokoodiryhmät"
description: "Tässä artikkelissa on yleistietoja tietokoodeista ja tietokoodiryhmistä sekä niiden käyttämisestä."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: af289f1c5612af8bc7406058d565649b75ac24d6
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="info-codes-and-info-code-groups"></a>Tietokoodit ja tietokoodiryhmät

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleistietoja tietokoodeista ja tietokoodiryhmistä sekä niiden käyttämisestä.

Tietokoodit tarjoavat tavan kerätä tietoja myyntipisteen rekisteriin. Voit käyttää tietokoodeja pyytämään kassanhoitajaa kirjoittamaan tiedot erilaisten myyntipisteen toimintojen aikana, kuten nimikkeen myynti, nimikkeen palautus tai asiakkaiden valinta. Kassat voivat valita syötteen luettelosta tai antaa sen koodina, numerona, päivämääränä tai tekstinä. Voit liittää tietokoodit ennalta määritettyihin myymälän toimiin, maksutapoihin, asiakkaisiin tai tiettyihin myyntipisteen tehtäviin. Voit käyttää tietokoodeja seuraavasti:
-   Kerää lisätietoja tapahtuman aikana, kuten lennon numeron ja palautuksen syy.
-   Kehote kassalle valita tiettyjen tuotteiden hintaluettelosta.
-   Linkitä alikoodi tietokoodiin, joka kehottaa kassaa syöttämään tiedon tietyn tehtävän suorituksen aikana. Esimerkiksi kun asiakas palauttaa tuotteen, voit pyytää kassanhoitajaa kysymään tuotepalautuksen syy. Tämän jälkeen voit käyttää alikoodeja syyluettelon näyttämiseen, josta kassanhoitaja voi valita.
-   Myy tuote tavallisessa myynnissä, alennetussa myynnissä tai ilmaisena tuotteena.
-   Kehota kassanhoitajaa kirjoittamaan arvo tai valitsemaan tarvittava arvo alikoodiluettelosta kassaa avattaessa ilman myynnin työvaiheen suorittamista.

## <a name="info-codes-group"></a>Tietokoodiryhmä
Voit luoda Dynamics 365 for Retailissa tietokoodien ryhmiä. Tietokoodiryhmät lisäävät joustavuutta ja antavat mahdollisuuden määrittää vähemmän tietokoodeja ja käyttää niitä monipuolisemmin. Voit käyttää tietokoodiryhmiä seuraavilla tavoilla:
-   Määritä vähemmän tietokoodeja ja käytä niitä helposti uudelleen. Tietokoodiryhmissä olevilla tietokoodeilla ei ole ennalta määritettyjä riippuvuuksia muissa tietokoodeissa. Voit sisällyttää samat kooditiedot useisiin tietokoodiryhmiin ja sitten käyttää priorisointia esittämään samat tietokoodit siinä järjestyksessä, joka vastaa kulloisiakin vaatimuksia.
-   Linkitä tietokoodit muihin tietokoodeihin tai tietokoodiryhmiin, jotta voit kerätä tietoja tuotteesta tai tapahtumasta määrittämättä erillistä tietokoodia tai linkitettyä tietokoodia jokaiselle skenaariolle.

## <a name="info-code-examples"></a>Tietokoodiesimerkkejä
**Esimerkki 1: Tietokoodien uudelleenkäyttö** Voit linkittää tietokoodit siten, että kun yksi tietokoodi käynnistyy, toinen koodi käynnistyy heti sen jälkeen. Kun esimerkiksi myyt tiettyjä tuotteita, kehota kassanhoitaja kysymään asiakkailta, haluavatko he ostaa paristoja ja tuotetakuun. Muiden tuotteiden kohdalla voit kehottaa kassanhoitajaa kysymään asiakkaalta, haluaako tämä ostaa paristoja, ja pyytämään asiakkaan postinumeron. Jos näissä tilanteissa luodaan linkitettyjä tietokoodeja, sinun on määritettävä tietokoodin jokainen muutos siten, että kassanhoitajaa kehotetaan pyytämään oikeat tiedot. Jos käytät tietokoodiryhmiä, yleiset tietokoodit, kuten paristojen pyytäminen, voidaan määrittää kerran ja sitten käyttää uudelleen useissa tietokoodiryhmissä. Voit käyttää myös priorisointia tietokoodiryhmissä määrittämään järjestyksen, jossa kehotteita näytetään.


**Esimerkki 2: Tietokoodien linkittäminen tietokoodiryhmiin** Kun myyt tiettyjä tuotteita, kuten mobiililaitteita, haluat aina kerätä tietyt tiedot, kuten puhelinnumeron, mobiililaitteen tunnuksen (MEID) ja sarjanumeron. Kuitenkin haluat myös kerätä eri tietoja taulutietokonesovellukseen kuin matkapuhelimeen. Voit määrittää tietokoodiryhmän, joka sisältää kehotteen puhelinnumeron, tunnuksen ja sarjanumeron kysymisestä ja linkittää sitten tietokoodiryhmän yksittäiseen tietokoodiin. Kun tuotetta koskeva infokoodi toteutuu, tietokoodiryhmä voidaan määrittää käynnistymään seuraavaksi, jotta voit kerätä yleisiä tietoja tarvitsematta määrittää useita linkitettyjä infokoodisarjoja kullekin laitteelle.





