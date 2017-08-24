--- 
title: "Nimikkeiden kattavuussääntöjen määrittäminen"
description: "Tämän menettelyn luomisessa käytetty esittely-yritys on USMF."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b34d2c35bc96cf75e9e699b835f7bcbbce1312b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="define-coverage-rules-for-items"></a>Nimikkeiden kattavuussääntöjen määrittäminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tässä menettelyssä näytetään, miten tietyn nimikkeen kattavuussäännöt luodaan ja kattavuusasetukset korvataan. Siinä näytetään myös, miten oletusvarastoasetukset määritetään.


## <a name="create-a-coverage-group"></a>Kattavuusryhmän luominen
1. Siirry Kattavuusryhmät-kohtaan.
2. Valitse Uusi.
3. Kirjoita Kattavuusryhmä-kenttään arvo.
4. Kirjoita arvo Nimi-kenttään.
5. Kirjoita Kalenteri-kenttään arvo.
    * Valitse kalenteri, jota pääsuunnittelu käyttää tämän ryhmän nimikkeiden täydennysehdotusten luomisessa.  
6. Valitse Kattavuuskoodi-kentässä vaihtoehto.
    * Valitse tämän menettelyn Tarve.  
7. Syötä Kattavuuden aikaraja (päivää) -kenttään 90.
    * Pääsuunnittelu luo tämän ryhmän nimikkeille täydennysehdotukset enintään 90 päivän ajalle tulevaisuuteen.  
8. Syötä Negatiiviset päivät -kenttään 1.
9. Syötä Positiiviset päivät -kenttään 1.
10. Laajenna tai tiivistä Muu-osa.
11. Syötä Tarvepäivään lisätty vastaanottomarginaali -kenttään 1.
    * Jos esimerkiksi vastaanottomarginaaliksi määritetään yksi päivä ja ostotilausrivi on ajoitettu vastaanotettavaksi 15.5., pääsuunnittelu laskee muutetuksi vastaanottopäiväksi 16.5.  
12. Syötä Tarvepäivästä vähennetty toimitusmarginaali -kenttään 1.
    * Jos esimerkiksi varmuusmarginaaliksi määritetään yksi päivä ja myyntitilausrivi on ajoitettu toimitettavaksi 15.5., pääajoitus laskee muutetuksi toimituspäiväksi 14.5.  
13. Syötä Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali -kenttään 1.
14. Valitse Tallenna.

## <a name="create-a-new-product"></a>Luo uusi tuote
1. Siirry Vapautetut tuotteet -kohtaan.
2. Valitse Uusi.
3. Kirjoita arvo Tuotenumero-kenttään.
4. Kirjoita arvo Tuotteen nimi -kenttään.
5. Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.
12. Etsi haluamasi tietue luettelosta ja valitse se.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Valitse OK.

## <a name="setup-default-order-settings"></a>Tilauksen oletusasetusten määrittäminen
1. Valitse toimintoruudussa Suunnitelma.
2. Valitse Tilauksen oletusasetukset.
3. Kirjoita Ostotoimipaikka-kenttään toimipaikka, jota käytetään oletusarvona ostotilausten luomisen yhteydessä.
4. Kirjoita Varastotoimipaikka-kenttään toimipaikka, joka on nimikkeen varasto.
5. Laajenna tai tiivistä Varasto-osa.
6. Määritä Useita-kohdan arvoksi 10.
7. Määritä Väh.tilausmäärä-kohdan arvoksi 10.
8. Määritä Enimm.tilausmäärä-kohdan arvoksi 100.
9. Määritä Vakiotilausmäärä-kohdan arvoksi 10.
10. Syötä Oston läpimenoaika -kenttään numero.
11. Valitse Työpäivät-valintaruutu tai poista sen valinta.
12. Valitse Tallenna.
13. Valitse Oletustilaustyyppi-kenttään Ostotilaus.
14. Valitse Tallenna.
15. Sulje sivu.
    * Sulje Tilauksen oletusasetukset -sivu.  

## <a name="add-an-item-to-a-coverage-group"></a>Nimikkeen lisääminen kattavuusryhmään
1. Laajenna tai tiivistä Suunnitelma-osa.
2. Avaa haku napsauttamalla Kattavuusryhmä-kentässä avattavan valikon painiketta.
3. Etsi luettelosta luomasi kattavuusryhmä.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="create-item-coverage-rules"></a>Nimikkeen kattavuussääntöjen luominen
1. Valitse toimintoruudussa Suunnitelma.
2. Valitse Nimikekattavuus.
3. Valitse Uusi.
4. Valitse Yleiset-välilehti.
5. Valitse Korvaa kattavuusryhmän asetukset -kohdan otsikossa valintaruutu.
6. Syötä Kattavuuden aikaraja (päivää) -kenttään 60.
    * Vaikka Tarve-kattavuusryhmän nimikkeet on suunniteltu 90 päivän ajalle, tämä nimike suunnitellaan 60 päivän ajalle.  
7. Syötä Negatiiviset päivät -kenttään 2.
8. Syötä Positiiviset päivät -kenttään 2.
9. Valitse Läpimenoaika-välilehti.
10. Valitse Osto-kohdan otsikon valintaruutu.
11. Syötä Ostoaika-kenttään 5.
12. Valitse Tallenna.


