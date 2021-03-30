---
title: Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota
description: Tässä menettelyssä käsitellään, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c25fb55afb01ed59b66045f24400e03e2ec60b2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238891"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Rekisteröi nimikkeet erikoisvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallinnan lisäprosessit. Vastaanottoassistentti tekee yleensä tämän tehtävän. 

Voit suorittaa tämän menettelyn USMF-demoyrityksen tiedoilla tai käyttää omia tietoja. Sinun on vahvistettava ostotilaus, jossa on avoin ostotilausrivi, ennen tämän opastuksen aloittamista. Rivin nimikkeen on oltava varastoitu, eikä se saa käyttää tuotevariantteja. Seurantadimensiot eivät myöskään saa olla käytössä. Nimike on myös liitettävä varastodimensioryhmään, jossa varastonhallintaprosessi on otettu käyttöön. Varastonhallintaprosessit on oltava otettuna käyttöön käytettävässä varastossa ja vastaanottoa on ohjattava käytettävässä toimipaikassa rekisterikilvillä. Jos käytössä on USMF, voit käyttää ostotilauksen luontiin yritystiliä 1001, varastoa 51 ja nimikettä M9200. 

Kirjoita muistiin luomasi ostotilauksen numero sekä ostotilausrivillä käytetty nimiketunnus ja toimipaikka.


## <a name="create-an-item-arrival-journal-header"></a>Luo nimikkeen saapumisen kirjauskansion otsikko
1. Valitse Nimikkeen saapuminen.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
    * Jos käytössä on USMF, voit syöttää arvoksi WHS. Jos käytät muita tietoja, kirjauskansiolla, jonka nimen valitsit, on oltava seuraavat ominaisuudet: Tarkista keräilysijainti -asetukseksi on määritettävä Ei ja Karanteeninhallinta-asetukseksi Ei.  
4. Kirjoita arvo Numero-kenttään.
5. Kirjoita arvo Toimipaikka-kenttään.
    * Valitse ostotilausrivillä käyttämäsi toimipaikka. Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena. Valitse USMF-tiedoissa varastoa 51, valitse toimipaikka 5.  
6. Kirjoita arvo Varasto-kenttään.
    * Valitse varasto, jota voi käyttää yhdessä valitsemasi toimipaikan kanssa. Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena. Jos käytät USMF-tietojen esimerkkiarvoja, valitse 51.  
7. Kirjoita arvo kenttään Sijainti.
    * Valitse sijainti valitsemastasi varastosta. Sijainnin on liityttävä sijaintiprofiiliin, jota rekisterikilpi hallitsee. Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena. Jos käytät USMF-tietojen esimerkkiarvoja, valitse Bulk-008.  
8. Napsauta Rekisterikilpi-kentässä alanuolta kakkospainikkeella ja valitse Näytä tiedot.
9. Valitse Uusi.
10. Kirjoita Rekisterikilpi-kenttään arvo.
    * Kirjoita arvo muistiin.  
11. Valitse Tallenna.
12. Sulje sivu.
13. Kirjoita Rekisterikilpi-kenttään arvo.
    * Anna juuri luodun rekisterikilven arvo. Se toimii oletusarvona, jota kaikki kirjauskansion rivit käyttävät oletuksena.  
14. Valitse OK.

## <a name="add-a-line"></a>Lisää rivi
1. Valitse Lisää rivi.
2. Kirjoita arvo Nimiketunnus-kenttään.
    * Anna ostotilausrivillä käyttämäsi nimiketunnus.  
3. Kirjoita numero Määrä-kenttään.
    * Anna rekisteröitävä määrä.  
    * Päivämäärä-kenttä määrittää päivämäärän, jolloin tämän nimikkeen käytettävissä oleva määrä rekisteröidään varastoon.  
    * Järjestelmä lisää erätunnuksen tiedot, jos erä voidaan yksilöivästi tunnistaa annetuista tiedoista. Muussa tapauksessa tiedot on lisättävä manuaalisesti. Tämä on pakollinen kenttä, joka linkittää tämän rekisteröinnin tietylle lähdeasiakirjariville.  

## <a name="complete-the-registration"></a>Suorita rekisteröinti
1. Valitse Vahvista.
    * Tämä tarkistaa, että kirjauskansio on valmis kirjattavaksi. Jos vahvistus epäonnistuu, virheet on korjattava ennen kirjausta kirjauskansioon.  
2. Valitse OK.
    * Tarkista sanoma, kun olet valinnut OK. Kyseisen sanoman pitäisi ilmoittaa, että kirjauskansio on OK.  
3. Valitse Kirjaa.
4. Valitse OK.
    * Tarkista sanomarivi, kun olet valinnut OK. Sanoman pitäisi ilmoittaa, että toiminto onnistui.  
5. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]