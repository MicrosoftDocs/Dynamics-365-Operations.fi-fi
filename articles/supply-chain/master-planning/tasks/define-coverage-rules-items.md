---
title: Nimikkeiden kattavuussääntöjen määrittäminen
description: Tässä menettelyssä näytetään, miten tietyn nimikkeen kattavuussäännöt luodaan ja kattavuusasetukset korvataan. Siinä näytetään myös, miten oletusvarastoasetukset määritetään.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15b0ad9faf2bcac25dec01a7ab44f804ad2345cd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567220"
---
# <a name="define-coverage-rules-for-items"></a>Nimikkeiden kattavuussääntöjen määrittäminen

[!include [banner](../../includes/banner.md)]

Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tässä menettelyssä näytetään, miten tietyn nimikkeen kattavuussäännöt luodaan ja kattavuusasetukset korvataan. Siinä näytetään myös, miten oletusvarastoasetukset määritetään.

## <a name="create-a-coverage-group"></a>Kattavuusryhmän luominen

Luo kattavuusryhmä seuraavasti:

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Pääsuunnittelu > Asetukset > Kattavuusryhmät**.
1. Valitse **Uusi**.
1. Kirjoita **Kattavuusryhmä**-kenttään arvo.
1. Kirjoita arvo **Nimi**-kenttään.
1. Kirjoita **Kalenteri**-kenttään arvo. Valitse kalenteri, jota pääsuunnittelu käyttää tämän ryhmän nimikkeiden täydennysehdotusten luomisessa.  
1. Valitse **Kattavuuskoodi**-kentässä vaihtoehto. Valitse tämän menettelyn Tarve.  
1. Syötä **Kattavuuden aikaraja (päivää)** -kenttään 90. Pääsuunnittelu luo tämän ryhmän nimikkeille täydennysehdotukset enintään 90 päivän ajalle tulevaisuuteen.  
1. Syötä **Negatiiviset päivät** -kenttään 1.
1. Syötä **Positiiviset päivät** -kenttään 1.
1. Laajenna tai tiivistä **Muu**-osa.
1. Syötä **Varmuusmarginaali vuorokausina** -osan **Tarvepäivään lisätty vastaanottomarginaali** -kenttään 1. Jos esimerkiksi vastaanottomarginaaliksi määritetään yksi päivä ja ostotilausrivi on ajoitettu vastaanotettavaksi 15.5., pääsuunnittelu laskee muutetuksi vastaanottopäiväksi 16.5.
1. Syötä **Tarvepäivästä vähennetty toimitusmarginaali** -kenttään 1. Jos esimerkiksi varmuusmarginaaliksi määritetään yksi päivä ja myyntitilausrivi on ajoitettu toimitettavaksi 15.5., pääajoitus laskee muutetuksi toimituspäiväksi 14.5.  
1. Syötä **Nimikkeen läpimenoaikaan lisätty uudelleenjärjestyksen marginaali** -kenttään 1.
1. Valitse **Tallenna**.

## <a name="create-a-new-product"></a>Luo uusi tuote

Luo uusi tuote seuraavasti:

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
1. Valitse **Uusi**.
1. Kirjoita arvo **Tuotenumero**-kenttään.
1. Kirjoita arvo **Tuotteen nimi**-kenttään.
1. Avaa haku valitsemalla **Nimikemalliryhmä**-kentässä avattavan valikon painike.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Avaa haku valitsemalla **Nimikeryhmä**-kentässä avattavan valikon painike.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike.
1. Etsi haluamasi tietue luettelosta ja valitse se.
1. Valitse luettelossa valitulla rivillä oleva linkki.
1. Valitse **OK**.

## <a name="set-up-default-order-settings"></a>Tilauksen oletusasetusten määrittäminen

Määritä tilauksen oletusasetukset seuraavasti:

1. Valitse **toimintoruudussa** **Suunnitelma**.
1. Valitse **Tilausasetukset**-kohdassa **Tilauksen oletusasetukset**.
1. Kirjoita **Ostotilaus**-kohdan **Oletustoimipaikka**-kenttään toimipaikka, jota käytetään oletusarvona ostotilausten luomisen yhteydessä.
1. Kirjoita **Oletusvarasto**-kenttään toimipaikka, joka on nimikkeen varasto.
1. Laajenna tai tiivistä **Varasto**-osa.
1. Kirjoita **Useita**-kenttään 10.
1. Kirjoita **Väh.tilausmäärä** -kenttään 10.
1. Kirjoita **Enimm.tilausmäärä** -kenttään 100.
1. Kirjoita **Vakiotilausmäärä** -kenttään 10.
1. Syötä **Oston läpimenoaika** -kenttään numero.
1. Valitse **Työpäivät**-valintaruutu tai poista sen valinta.
1. Valitse **Tallenna**.
1. Valitse **Oletustilaustyyppi**-kenttään Ostotilaus.
1. Valitse **Tallenna**.
1. Sulje sivu. Sulje Tilauksen oletusasetukset -sivu.  

## <a name="add-an-item-to-a-coverage-group"></a>Nimikkeen lisääminen kattavuusryhmään

Lisää nimike kattavuusryhmään seuraavasti:

1. Laajenna tai tiivistä **Suunnitelma**-osa.
1. Avaa haku valitsemalla avattavan valikon painike **Kattavuusryhmä**-kentässä.
1. Etsi luettelosta luomasi **Kattavuusryhmä**.
1. Valitse luettelossa valitulla rivillä oleva linkki.

## <a name="create-item-coverage-rules"></a>Nimikkeen kattavuussääntöjen luominen

Luo nimikkeen kattavuussäännöt seuraavasti:

1. Valitse **toimintoruudussa** **Suunnitelma**.
1. Valitse **Kattavuus**-kohdassa **Nimikkeen kattavuus**.
1. Valitse **Uusi**.
1. Valitse **Yleinen**-välilehti.
1. Valitse **Korvaa kattavuusryhmän asetukset** -kohdan otsikossa valintaruutu.
1. Syötä **Kattavuuden aikaraja (päivää)** -kenttään 60. Vaikka Tarve-kattavuusryhmän nimikkeet on suunniteltu 90 päivän ajalle, tämä nimike suunnitellaan 60 päivän ajalle.  
1. Syötä **Negatiiviset päivät** -kenttään 2.
1. Syötä **Positiiviset päivät** -kenttään 2.
1. Valitse **Läpimenoaika**-välilehti.
1. Valitse **Osto**-kohdan otsikon valintaruutu.
1. Syötä **Ostoaika**-kenttään 5.
1. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]