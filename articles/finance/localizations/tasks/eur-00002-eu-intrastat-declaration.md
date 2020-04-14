---
title: EUR-00002 EU Intrastat -ilmoituksen luominen
description: Tässä menettelyssä käydään läpi vaiheet, joissa viedään Intrastat-ilmoituksen sähköisessä tiedostomuodossa ja esikatsellaan ilmoitustiedot Excel-muodossa.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2aba5caaaf0fbee511e1a293b09fa8301bb6831
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145263"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 EU Intrastat -ilmoituksen luominen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käydään läpi vaiheet, joissa viedään Intrastat-ilmoituksen sähköisessä tiedostomuodossa ja esikatsellaan ilmoitustiedot Excel-muodossa. 

Ennen kuin suoritat tämän menettelyn, tapahtumat on siirrettävä Intrastatiin. 

Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.


## <a name="import-configurations-with-settings"></a>Asetuksia sisältävien konfiguraatioiden tuonti
1. Valitse Työtilat > Sähköinen raportointi
2. Valitse Aseta aktiiviseksi.
3. Valitse Säilöt.
4. Valitse Avaa.
5. Avaa Konfiguraation nimi -sarakkeen suodatin.
6. Käytä suodatinta Konfiguraation nimi -kentässä niin, että arvo on "Intrastat (DE)" ja suodatinoperaattori Alkaa.
    * Valitse yrityksesi toimintamaata vastaava konfiguraation nimi. Näissä toimintaohjeissa käytetään esimerkkinä saksalaista yritystä (DEMF); tämän vuoksi tulee valita "Intrastat (DE)".  
    * Valitse Tuo ja valitse sitten Kyllä.  
7. Avaa Konfiguraation nimi -sarakkeen suodatin.
8. Käytä suodatinta Konfiguraation nimi -kentässä niin, että arvo on "Intrastat-raportti" ja suodatinoperaattori Alkaa.
    * Valitse Tuo ja valitse sitten Kyllä.  

## <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit
1. Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit
2. Laajenna Sähköinen raportointi -osa.
3. Anna tai valitse Tiedostomuodon yhdistäminen -kentässä arvoksi Intrastat (DE).
4. Anna tai valitse Raporttimuodon yhdistäminen -kentässä arvoksi Intrastat-raportti.
5. Laajenna Pyöristyssäännöt-osa.
    * Pyöristyssäännöt tulee määrittää maasi/alueesi Intrastat-raportoinnin käytäntöjen mukaisiksi.  
6. Syötä Pyöristyssääntö-kenttään numero.
    * Anna pyöristystarkkuus, esimerkiksi 0,01.  
7. Syötä Summan desimaalien määrä -kenttään haluamasi luku.
    * Kirjoita esimerkiksi 2.  
8. Valitse vaihtoehto Pyöristys, alle 1 kg -kentässä.
    * Valitse esimerkiksi "Pyöristys, enintään 1 kg".  
9. Syötä Pyöristyssääntö-kenttään numero.
    * Kirjoita esimerkiksi 1 kokonaisluvun pyöristyksen painotukseksi.  
10. Laajenna Vähimmäisraja-osa.
11. Syötä numero Paino-kenttään.
    * Määritä vähimmäispainoksi esimerkiksi "10".  
12. Lisää Summa-kenttään numero.
    * Määritä vähimmäismääräksi esimerkiksi "200".  
13. Syötä tai valitse arvo Kauppatavara-kentässä.

## <a name="set-up-compression-of-intrastat"></a>Määritä Intrastatin tiivistysasetukset
1. Valitse Vero > Asetukset > Ulkomaankauppa > Intrastatin tiivistys.
2. Valitse Poista.
3. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse esimerkiksi Kauppatavara Käytettävissä-osasta.  
4. ValitseLisää.

## <a name="generate-intrastat-declaration"></a>Intrastat-ilmoituksen luominen
1. Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat
2. Valitse Vahvista.
    * Oikeellisuustarkistus suoritetaan Ulkomaankaupan parametrit -sivun Tarkista asetukset -kentän mukaisesti.  
3. Valitse OK.
4. Valitse Päivitä.
5. Valitse Vähimmäisraja.
6. Syötä päivämäärä Aloituspäivä-kenttään.
    * Syötä kenttään esimerkiksi 1. tammikuuta 2015.  
7. Valitse Tiivistä-kentässä Kyllä.
8. Syötä päivämäärä Päättymispäivä-kenttään.
    * Syötä kenttään esimerkiksi 31. tammikuuta 2015.  
9. Valitse OK.
10. Valitse Päivitä.
11. Valitse Tiivistä.
    * Tämä pakkaus tapahtuu sen mukaan, miten Intrastatin pakkausasetukset on määritetty.  
12. Syötä päivämäärä Aloituspäivä-kenttään.
    * Syötä kenttään esimerkiksi 1. tammikuuta 2015.  
13. Syötä päivämäärä Päättymispäivä-kenttään.
    * Syötä kenttään esimerkiksi 31. tammikuuta 2015.  
14. Valitse OK.
15. Valitse Päivitä.
16. Valitse Muodosta uudestaan järjestysnumerot.
17. Valitse OK.
18. Valitse Tulostus.
19. Valitse Raportti.
20. Kirjoita Aloituspäivämäärä-kenttään raportointikauden ensimmäinen päivä.
    * Aseta päivämääräksi esim. 1. tammikuuta 2015.  
21. Kirjoita päivämäärä Päivämäärään-kenttään.
    * Syötä kenttään esimerkiksi 31. tammikuuta 2015.  
22. Valitse Luo tiedosto -kentässä Kyllä.
23. Kirjoita arvo Tiedostonimi-kenttään.
24. Valitse Luo raportti -kentässä Kyllä.
25. Kirjoita arvo Raportin nimi -kenttään.
26. Valitse vaihtoehto kentässä Suunta.
    * Valitse esimerkiksi Lähtevät.  
27. Valitse OK.

