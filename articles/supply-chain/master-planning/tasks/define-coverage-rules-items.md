---
title: Nimikkeiden kattavuussääntöjen määrittäminen
description: Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427090"
---
# <a name="define-coverage-rules-for-items"></a>Nimikkeiden kattavuussääntöjen määrittäminen

[!include [banner](../../includes/banner.md)]

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tässä menettelyssä näytetään, miten tietyn nimikkeen kattavuussäännöt luodaan ja kattavuusasetukset korvataan. Siinä näytetään myös, miten oletusvarastoasetukset määritetään.


## <a name="create-a-coverage-group"></a>Kattavuusryhmän luominen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Pääsuunnittelu > Asetukset > Kattavuusryhmät**.
2. Valitse **Uusi**.
3. Kirjoita **Kattavuusryhmä**-kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Kirjoita **Kalenteri**-kenttään arvo. Valitse kalenteri, jota pääsuunnittelu käyttää tämän ryhmän nimikkeiden täydennysehdotusten luomisessa.  
6. Valitse **Kattavuuskoodi**-kentässä vaihtoehto. Valitse tämän menettelyn Tarve.  
7. Syötä **Kattavuuden aikaraja (päivää)** -kenttään 90. Pääsuunnittelu luo tämän ryhmän nimikkeille täydennysehdotukset enintään 90 päivän ajalle tulevaisuuteen.  
8. Syötä **Negatiiviset päivät** -kenttään 1.
9. Syötä **Positiiviset päivät** -kenttään 1.
10. Laajenna tai tiivistä **Muu**-osa.
11. Syötä **Varmuusmarginaali vuorokausina** -osan **Tarvepäivään lisätty vastaanottomarginaali** -kenttään 1. Jos esimerkiksi vastaanottomarginaaliksi määritetään yksi päivä ja ostotilausrivi on ajoitettu vastaanotettavaksi 15.5., pääsuunnittelu laskee muutetuksi vastaanottopäiväksi 16.5.  
12. Syötä **Tarvepäivästä vähennetty toimitusmarginaali** -kenttään 1. Jos esimerkiksi varmuusmarginaaliksi määritetään yksi päivä ja myyntitilausrivi on ajoitettu toimitettavaksi 15.5., pääajoitus laskee muutetuksi toimituspäiväksi 14.5.  
13. Syötä **Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali** -kenttään 1.
14. Valitse **Tallenna**.

## <a name="create-a-new-product"></a>Luo uusi tuote
1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Tuotenumero**-kenttään.
4. Kirjoita arvo **Tuotteen nimi**-kenttään.
5. Avaa haku valitsemalla **Nimikemalliryhmä**-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Avaa haku valitsemalla **Nimikeryhmä**-kentässä avattavan valikon painike.
9. Etsi haluamasi tietue luettelosta ja valitse se.
10. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
11. Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike.
12. Etsi haluamasi tietue luettelosta ja valitse se.
13. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
14. Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike.
15. Etsi haluamasi tietue luettelosta ja valitse se.
16. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
17. Valitse **OK**.

## <a name="setup-default-order-settings"></a>Tilauksen oletusasetusten määrittäminen
1. Valitse **toimintoruudussa** **Suunnitelma**.
2. Valitse **Tilausasetukset**-kohdassa **Tilauksen oletusasetukset**.
3. Kirjoita **Ostotilaus**-kohdan **Oletustoimipaikka**-kenttään toimipaikka, jota käytetään oletusarvona ostotilausten luomisen yhteydessä.
4. Kirjoita **Oletusvarasto**-kenttään toimipaikka, joka on nimikkeen varasto.
5. Laajenna tai tiivistä **Varasto**-osa.
6. Kirjoita **Useita**-kenttään 10.
7. Kirjoita **Väh.tilausmäärä** -kenttään 10.
8. Kirjoita **Enimm.tilausmäärä** -kenttään 100.
9. Kirjoita **Vakiotilausmäärä** -kenttään 10.
10. Syötä **Oston läpimenoaika** -kenttään numero.
11. Valitse **Työpäivät**-valintaruutu tai poista sen valinta.
12. Valitse **Tallenna**.
13. Valitse **Oletustilaustyyppi**-kenttään Ostotilaus.
14. Valitse **Tallenna**.
15. Sulje sivu. Sulje Tilauksen oletusasetukset -sivu.  

## <a name="add-an-item-to-a-coverage-group"></a>Nimikkeen lisääminen kattavuusryhmään
1. Laajenna tai tiivistä **Suunnitelma**-osa.
2. Avaa haku napsauttamalla **Kattavuusryhmä**-kentässä avattavan valikon painiketta.
3. Etsi luettelosta luomasi **Kattavuusryhmä**.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="create-item-coverage-rules"></a>Nimikkeen kattavuussääntöjen luominen
1. Valitse **toimintoruudussa** **Suunnitelma**.
2. Valitse **Kattavuus**-kohdassa **Nimikkeen kattavuus**.
3. Valitse **Uusi**.
4. Valitse **Yleiset**-välilehti.
5. Valitse **Korvaa kattavuusryhmän asetukset** -kohdan otsikossa valintaruutu.
6. Syötä **Kattavuuden aikaraja (päivää)** -kenttään 60. Vaikka Tarve-kattavuusryhmän nimikkeet on suunniteltu 90 päivän ajalle, tämä nimike suunnitellaan 60 päivän ajalle.  
7. Syötä **Negatiiviset päivät** -kenttään 2.
8. Syötä **Positiiviset päivät** -kenttään 2.
9. Valitse **Läpimenoaika**-välilehti.
10. Valitse **Osto**-kohdan otsikon valintaruutu.
11. Syötä **Ostoaika**-kenttään 5.
12. Valitse **Tallenna**.

