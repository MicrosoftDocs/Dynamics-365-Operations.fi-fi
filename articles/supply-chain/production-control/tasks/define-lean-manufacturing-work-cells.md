---
title: Määritä lean-valmistuksen työsolut
description: Työsolun on erityinen resurssiryhmä, jota voidaan käyttää Lean-valmistuksen prosessitehtävissä.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, InventLocationIdLookup, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96c65690b7d67bffc2cf09c4ea34c84755f8530a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001546"
---
# <a name="define-lean-manufacturing-work-cells"></a>Määritä lean-valmistuksen työsolut

[!include [banner](../../includes/banner.md)]

Työsolun on erityinen resurssiryhmä, jota voidaan käyttää Lean-valmistuksen prosessitehtävissä. Työsoluilla on syöttö- ja tuotossijainnit sekä tuotantovirtamalliin perustuva kapasiteettimääritys. Lisätietoja Lean-valmistuksen työsolujen ja kapasiteettilaskelmien peruskäsitteistä on Lean-valmistusta käsittelevissä teknisissä raporteissa. Tämän menettelyn luonnissa käytettiin USMF-yrityksen demotietoja.


## <a name="create-a-work-cell"></a>Luo työsolu. 
1. Valitse Organisaation hallinto > Resurssit > Resurssiryhmät.
2. Valitse Uusi.
3. Kirjoita arvo Resurssiryhmä-kenttään.
    * Työsolun tunnus on yleensä yrityskohtainen järjestelmäkoodi.  
4. Kirjoita arvo Kuvaus-kenttään.
    * Kuvaus sisältää työsolun nimen tai otsikon.  
5. Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.
    * Työsolun sijaitsee tietyssä toimipaikassa. Sekä saapuvan ja lähtevän varaston että sijainnin on oltava kyseisessä toimipaikassa.  
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
7. Avaa haku napsauttamalla Tuotantoyksikkö-kentässä avattavan valikon painiketta.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Valitse tuotantoyksikkö, jota tämä työsolu kuuluu.  
9. Valitse Työsolu-valintaruutu.
    * Resurssiryhmän käyttö Lean-työsoluna edellyttää, että Työsolu-valintaruutu on valittu.  Huomaa, että tätä ominaisuutta ei voi muuttaa, kun resurssiryhmä on luotu.  
10. Avaa haku napsauttamalla Syöttövarasto-kentässä avattavan valikon painiketta.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Kirjanpito- ja materiaalivalvonnan vuoksi työnohjaukseen vaiheistettu materiaali kohdistetaan yleensä tiettyyn virtuaalivarastoon. Jos kuitenkin haluat täyttää sijainnit käyttämällä varastotyötä, niiden on oltava osa vastaanottavaa raaka-ainevarastoa.  
12. Avaa haku napsauttamalla Syöttösijainti-kentässä avattavan valikon painiketta.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Huomaa, että prosessitehtävässä syöttösijainti voidaan korvata yleisesti tai tietyllä tuotteella tai tuotevariantilla määrittämällä prosessitehtävää syöttävät keräilytehtävät. Työsolun syöttösijainti ei voi olla rekisterikilpivalvottu.  
14. Avaa haku napsauttamalla Tuotosvarasto-kentässä avattavan valikon painiketta.
15. Etsi haluamasi tietue luettelosta ja valitse se.
    * Jos tuotantovirroissa tai tuotantoriveillä on useita tehtäviä, kyse on usein seuraavan työsolun syöttövarastosta tai myynti- tai siirtovarastosta, johon tuote tavallisesti siirretään tuotantoprosessin jälkeen. Muista Lean-valmistusprosessia mallinnettaessa, että kuljetus on yleensä hävikkiä samoin kuin kuljetuksen raportointi.  
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Avaa haku napsauttamalla Tuotossijainti-kentässä avattavan valikon painiketta.
    * jos tuotantovirrassa on useita prosessitehtäviä, tämä on usein seuraavan työsolun syöttösijainti.  
18. Etsi haluamasi tietue luettelosta ja valitse se.
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
20. Laajenna tai tiivistä Toiminto-osa.
    * Ajoaikaluokka on ilmoitettava, jotta Lean-valmistuksen kanban-töiden kustannuslaskenta ja käsittely on mahdollista.  
21. Avaa haku napsauttamalla Ajoaikaluokka-kentässä avattavan valikon painiketta.
22. Etsi haluamasi tietue luettelosta ja valitse se.
    * Ajoajan kustannusluokkaa käytetään standardi- ja jälkikustannuslaskennassa.  
23. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
24. Laajenna tai tiivistä Kalenterit-osa.
25. ValitseLisää.
26. Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.
27. Etsi haluamasi tietue luettelosta ja valitse se.
    * Annetun toimipaikan työsolut käyttävät yleensä samaa työaikakalenteria. Jos työsoluilla voi olla yksittäiset työajat, työsolulle on ehkä luotava oma työaikakalenteri. Huomaa, että Lean-työsolussa käytettävässä kalenterissa on oltava normaali työaika määritettynä, koska kapasiteettimääritys liittyy yleensä työpäivän normaaliin työaikaan.  
28. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
29. Laajenna tai tiivistä Työsolun kapasiteetti -osa.
30. ValitseLisää.
31. Avaa haku napsauttamalla Tuotantovirtamalli-kentässä avattavan valikon painiketta.
32. Etsi haluamasi tietue luettelosta ja valitse se.
    * Tämä menettely edellyttää tuotantovirtamallia Tuotantokapasiteetti, jotta tuotantoteho voidaan näyttää.  
33. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
34. Valitse vaihtoehto Kapasiteettikausi-kentässä.
    * Vaihtoehdot: Tavallinen työpäivä – Kapasiteetti ilmoitetaan työsolun työaikakalenterin tavallisen työpäivän pituutena. Kunkin päivän todellinen työaika määritetään kalenterista, jonka perusteella lasketaan käytettävissä oleva tehollinen kapasiteetti.   Viikko – Sallii viikkokapasiteetin. Todellisen työajan oikaisua ei tehdä.   Kuukausi – Sallii kuukausikapasiteetin. Todellisen kapasiteetin oikaisua ei tehdä.   Yleensä tavallista työpäivää käytetään päivittäiselle kaudelle, kun taas viikkokapasiteettia käytetään viikoittaisille kapasiteettikausille.  
35. Lisää Tuotantokapasiteetin keskimääräinen määrä -kenttään numero.
    * Huomaa, että Lean-työvaihetta ei koskaan määritetä suurimmalle mahdolliselle kapasiteetille ihanteellisissa olosuhteissa. Sen sijaan kapasiteetti pitäisi aina määrittää tyypillisissä olosuhteissa tehtäville työtehtäville.  
36. Avaa haku napsauttamalla Yksikkö -kentässä avattavan valikon painiketta.
37. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
38. Ratkaise muutokset yksikössä.

## <a name="add-a-financial-dimension"></a>Lisää taloushallinnon dimensio
1. Laajenna tai tiivistä Taloushallinnon dimensiot -osa.
    * Huomaa, että tuotantovirrassa määritetyt taloushallinnon dimensiot ohittavat annetun työsolun taloushallinnon dimension.    Valittavat taloushallinnon dimensiot määräytyvät järjestelmän taloushallinnon dimensioiden määritysten mukaan. Seuraavat vaiheet vastaavat USMF-yrityksen demotietojoukkoja. Muita tietoja käytettäessä kyseisiä vaiheita ei ehkä käytetä.  
2. Avaa haku valitsemalla CostCenter-kentässä avattavan valikon painike.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Lean-työsoluissa valittavat dimensiot määräytyvät sen mukaan, miten taloushallinnon dimensiot on toteutettu tietyn yrityksen kirjanpitomallissa.  
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Avaa haku valitsemalla ItemGroup-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="save"></a>Tallenna
1. Valitse Tallenna.

