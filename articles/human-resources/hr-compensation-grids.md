---
title: Kompensaatioruudukoiden määrittäminen
description: Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d5ada0817dd73caad38bb2e50302869857c71d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418312"
---
# <a name="set-up-compensation-grids"></a>Kompensaatioruudukoiden määrittäminen

Kompensaatioruudukoiden avulla voidaan määrittää ja ylläpitää kiinteiden kompensaatiosuunnitelmien palkkarakenteita. Kompensaatioruudukoita voidaan jakaa useiden suunnitelmien välillä tai ne voidaan kopioida uutta kompensaatiosuunnitelmaa luotaessa.  Tasot ja viitepisteet on määritettävä ennen kompensaatioruudukon luontia. Tässä esimerkissä luodaan uusi Palkkaluokka-tyyppinen kompensaatioruudukko käyttämällä esittelytiedot tasoissa ja viitepisteissä demotietoja. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Määritä kompensaatioruudukkoa koskevat tiedot
1. Valitse Henkilöstöhallinto > Kompensaatio > Kiinteä kompensaatio > Kompensaatioruudukot.
2. Valitse Uusi.
3. Kirjoita Ruudukko-kenttään arvo.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse vaihtoehto Tyyppi-kentässä.
6. Anna tai valitse arvo Viitemääritykset-kentässä.
7. Anna tai valitse Valuutta-kentässä arvo.
8. Kirjoita arvo Valuutta-kenttään.
9. Syötä päivämäärä Voimaantulopäivä-kenttään.

## <a name="add-levels-to-the-compensation-structure"></a>Lisää tasoja kompensaatiorakenteeseen
1. Valitse Kompensaatiorakenne.
2. Merkitse valittu rivi luettelossa.
3. Anna tai valitse Taso-kentässä arvo.
4. Valitse Uusi.
5. Merkitse valittu rivi luettelossa.
6. Anna tai valitse Taso-kentässä arvo.
7. Valitse Uusi.
8. Merkitse valittu rivi luettelossa.
9. Anna tai valitse Taso-kentässä arvo.
10. Valitse Uusi.
11. Merkitse valittu rivi luettelossa.
12. Anna tai valitse Taso-kentässä arvo.
13. Valitse Uusi.
14. Merkitse valittu rivi luettelossa.
15. Anna tai valitse Taso-kentässä arvo.

## <a name="fill-in-the-compensation-structure-with-values"></a>Täytä kompensaatiorakenteen arvot
1. Merkitse valittu rivi luettelossa.
    * Kompensaatioarvot voidaan lisätä tässä vaiheessa taulun kenttiin. Joukkomuutos-toiminnolla voidaan vaihtoehtoisesti täyttää kätevästi useita kenttiä ja suorittaa peruslaskutoimituksia.  
2. Valitse Joukkomuutos.
    * Tässä ruudukossa käytetään ensiksi ensimmäisen tason keskipisteen arvoa kaikkiin taulun kenttiin. Kompensaatiomatriisi tulee perustumaan siihen.  
3. Valitse Oikaisulaji-kentässä vaihtoehto.
4. Syötä Oikaisusumma-kenttään numero.
5. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
6. Valitse Sovella ruudukkoon.
    * Seuraavaksi kasvatetaan joukkomuutostoiminnolla kunkin seuraavan tason summia tietyllä prosentilla tai summalla. Tässä esimerkissä jokaisella luokalla on 12,5 prosentin hajonta keskipisteiden välillä.  
7. Valitse Oikaisulaji-kentässä vaihtoehto.
8. Syötä Oikaisusumma-kenttään numero.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Etsi haluamasi tietue luettelosta ja valitse se.
11. Etsi haluamasi tietue luettelosta ja valitse se.
12. Etsi haluamasi tietue luettelosta ja valitse se.
13. Valitse Sovella ruudukkoon.
14. Etsi haluamasi tietue luettelosta ja valitse se.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Etsi haluamasi tietue luettelosta ja valitse se.
17. Valitse Sovella ruudukkoon.
18. Etsi haluamasi tietue luettelosta ja valitse se.
19. Etsi haluamasi tietue luettelosta ja valitse se.
20. Valitse Sovella ruudukkoon.
21. Etsi haluamasi tietue luettelosta ja valitse se.
22. Valitse Sovella ruudukkoon.
    * Nyt joukkomuutostoiminnolla muutetaan kunkin tason pienintä ja suurinta viitepistettä. Tässä esimerkissä käytetään 50 prosentin hajontaa, joten pienintä viitepistettä vähennetään 20 prosentilla ja suurinta suurennetaan 20 prosentilla.  
23. Syötä Oikaisusumma-kenttään numero.
24. Anna tai valitse arvo Viitepiste-kentässä.
25. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
26. Valitse Sovella ruudukkoon.
27. Syötä Oikaisusumma-kenttään numero.
28. Anna tai valitse arvo Viitepiste-kentässä.
29. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
30. Valitse Sovella ruudukkoon.



[!INCLUDE[footer-include](../includes/footer-banner.md)]