---
title: Jatkuvuusohjelman käyttäminen
description: Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267401"
---
# <a name="using-continuity-program"></a>Jatkuvuusohjelman käyttäminen

[!include [banner](../includes/banner.md)]

Näissä toimintaohjeissa neuvotaan, miten jatkuvuusohjelman avulla tehdään myyntejä ja käsitellään niihin liittyviä myyntitilauksia. Käyttäjä on määritettävä puhelinkeskuksen käyttäjäksi, jotta tämän menettelyn voi suorittaa. Menettely käyttää esittelytietojen USRT-yritystä.

1. Valitse Retail ja Commerce > Asiakkaat > Asiakaspalvelu.
2. Kirjoita SearchText-kenttään "Karen" ja paina sitten sarkainnäppäintä.
    * Tarkennettu haku -valintaikkunan tulisi aueta. Jos näin ei tapahdu, valitse Etsi kentän oikealla puolella.  
3. Merkitse valittu rivi luettelossa.
    * Tuloksissa tulisi olla vain yksi rivi nimellä Karen Berg. Valitse rivi napsauttamalla valintamerkkiä ruudukon vasemmassa laidassa.  
4. Klikkaa Valitse.
5. Valitse Uusi myyntitilaus.
    * Ota muistiin myyntitilauksen numero. Tarvitset sitä myöhemmin.  
6. Kirjoita Nimiketunnus-kenttään 88000 ja paina sitten sarkainnäppäintä.
    * Tämä on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.  
7. Valitse Valmis.
8. Kirjoita Maksutapa-kenttään "Visa".
9. Valitse Lisää luottokortti.
    * Anna pakolliset luottokorttitiedot tällä sivulla.  
10. Valitse OK.
11. Laajenna Maksu-osa.
    * Jotta puhelinkeskus voi lähettää tilauksen, tilaukselle on syötettävä maksuja.  
12. Valitse OK.
13. Valitse Lähetä.
    * Jatkuvuustilauksen luonti on nyt valmis. Seuraavaksi ajat kaksi eräprosessia, jotka käsittelevät jatkuvuustilaukset.  
14. Sulje sivu.
15. Valitse Retail ja Commerce > Jatkuvuus > Käsittele jatkuvuusmaksut.
16. Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.
17. Valitse OK.
18. Valitse Retail ja Commerce > Jatkuvuus > Luo jatkuvuuden alitilaukset.
    * Tämä prosessi luo uusia myyntitilauksia, jotka perustuvat jatkuvuusohjelmasi asetuksiin.  
19. Kirjoita Jatkuvuusnimike-kenttään 88000 ja paina sitten sarkainnäppäintä.
    * Nimike 88000 on jatkuvuusnimike USRT-yrityksen esittelytiedoissa.  
20. Syötä tai valitse arvo kentässä Myyntitilaus.
    * Anna aiemmin ohjeessa muistiin ottamasi myyntitilauksen numero. Tämä vähentää ohjeiden suoritusaikaa huomattavasti. Myyntitilaus-kenttä on valinnainen – voit käsitellä kaikki yhden ohjelman tilaukset.  
21. Valitse OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
