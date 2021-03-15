---
title: Alusta varaston varastotasoja
description: Tässä menettelyssä selitetään, miten käytettävissä oleva varasto päivitetään manuaalisesti varastosiirron kirjauskansion avulla.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6934fc8142a589532cbd9d360ca0f8276456b20e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011544"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Alusta varaston varastotasoja

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selitetään, miten käytettävissä oleva varasto päivitetään manuaalisesti varastosiirron kirjauskansion avulla. (Käytettävissä oleva varasto voidaan päivittää myös tuomatta tietoyksiköiden tapahtumat.) Voit suorittaa tämän opastuksen USMF-yrityksen demotiedoissa, jolloin kaikki edellytykset, kuten kirjauskansion nimi, nimikeasetukset, kirjausprofiilit ja tilit ovat käytettävissä. Opastuksessa ehdotetaan käytettäville nimikkeelle ja dimensioille tiettyjä arvoja. Jos valitset toisen nimikkeen, eri dimensioiden arvot on ehkä annettava.

1. Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeet > Siirto.
2. Valitse Uusi.
3. Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.
4. Valitse IMov.
    * On hyvä käytännön mukaista käyttää erilaisia kirjauskansion nimimalleja eri liiketoimintatarkoituksiin.  
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Määritä Vastatili-kenttään arvo 140200.
    * Tämä vastatili on kirjauskansiorivien oletustili. Oletuksen voi korvat määrittämällä rivikohtaisesti eri vastatilit.  
7. Valitse OK.
8. Valitse Uusi.
9. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
10. Valitse nimike A0001.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Valitse Varastodimensiot-välilehti.
13. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
14. Valitse toimipaikka 1.
15. Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.
16. Valitse varasto 13.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.
19. Valitse sijainti 13.
20. Kirjoita numero Määrä-kenttään.
21. Valitse Tallenna.
22. Valitse Kirjaa.
23. Valitse Siirrä kaikki kirjausvirheet uuteen kirjauskansioon -valintaruutu tai poista sen valinta.
    * Jos tämä vaihtoehto otetaan käyttöön, kaikki rivit, joiden kirjaus epäonnistui, kopioidaan uuteen kirjauskansioon. Voit korjata ongelmat tämän lokin tietojen perusteella ja kirjata rivit uudelleen.  
24. Valitse OK.
25. Sulje sivu.
26. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]