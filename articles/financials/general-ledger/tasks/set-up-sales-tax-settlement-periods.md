--- 
title: "Määritä arvonlisäveron tilityskaudet"
description: "Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava."
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 81214cc52b1488bb70ac5fd6ccc817f6f979163d
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.contentlocale: fi-fi
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a>Määritä arvonlisäveron tilityskaudet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava. Tilitysprosessi voidaan suorittaa tietyn päivämäärävälin tilityskaudelle. Kaikki tilityskauteen liittyvät verokoodit on tilitettävä. Liittyvän arvonlisäveroviranomaisen määrityksestä riippuen verovelka kirjataan joko toimittajan tilille tai kirjanpitotilille.



Tässä tehtävässä käytetään esittely-yritystä USMF.



1. Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveron tilityskaudet.
2. Valitse Uusi.
3. Kirjoita arvo Tilityskausi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Valitse Viranomainen-kentästä arvonlisäveroviranomainen, joka vastaanottaa tilityskaudelle luodut raportit ja maksut.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Maksuehdot-kentässä avattavan valikon painike.
    * Liittyvä arvonlisäveroviranomainen voidaan määrittää toimittajaksi. Arvonlisäveron tilitys luo avoimen toimittajan laskun. Maksuehdot määrittävät avoimen toimittajan laskun eräpäivän.  
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Valitse tilityskauden välien tyyppi.
12. Syötä kausivälien yksiköiden määrä kautta kohti. Esimerkiksi neljännesvuosi sisältää 3 kuukautta.
13. Valitse Käytä arvonlisäveron tilitykseen eräprosessia -valintaruutu tai poista sen valinta.
    * Tilityskauden tilitysprosessi voidaan käsitellä taustalla erätyönä. Tätä suositellaan, jos kausiväli sisältää paljon verotapahtumia.  
14. Valitse Estä verotapahtumien vastakirjauksien luonti -valintaruutu tai poista sen valinta.
    * Järjestelmä luo oletusarvoisesti verotapahtumien vastakirjauksia selvitysprosessin aikana, mikä voi heikentää suorituskykyä, jos kausiväliin sisältyy suuri määrä verotapahtumia. Estä verotapahtumien vastakirjauksien luonti valitsemalla tämä valintaruutu.
15. Laajenna Kausivälit-välilehti.
16. ValitseLisää.
17. Merkitse valittu rivi luettelossa.
18. Syötä päivämäärä Päivämäärästä-kenttään.
19. Kirjoita päivämäärä Päivämäärään-kenttään.
20. Valitse Uusi kausiväli.
    * Kun ensimmäinen kausiväli on syötetty, uudet kaudet voidaan luoda automaattisesti. Voit siirtyä takaisin ja lisätä tarvittaessa uusia kausivälejä.  
21. Sulje sivu.


