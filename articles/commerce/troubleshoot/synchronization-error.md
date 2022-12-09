---
title: Asynkronisten tilausten synkronoinnin ongelmat
description: Tässä artikkelissa kuvaillaan asynkronisen tilauksen luonnin virheitä Microsoft Dynamics 365 Commercessa ja annetaan vianmääritysohjeita, jotta järjestelmän käyttäjät ja kumppanit ymmärtävät, mikä meni vikaan.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815753"
---
# <a name="asynchronous-order-synchronization-issues"></a>Asynkronisten tilausten synkronoinnin ongelmat

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvaillaan asynkronisen tilauksen luonnin virheitä Microsoft Dynamics 365 Commercessa ja annetaan vianmääritysohjeita, jotta järjestelmän käyttäjät ja kumppanit ymmärtävät, mikä meni vikaan.

## <a name="symptom"></a>Oire

Dynamics 365 Commercen sähköisestä kaupankäynnistä tai myyntipisteestä (POS) luodut asynkroniset tilaukset eivät näy Commerce headquartersissa.

## <a name="troubleshooting"></a>Vianmääritys

Tilauksen luominen voi epäonnistua headquartersissa eri syistä sen mukaan, missä vaiheessa tilauksen luontiprosessi epäonnistuu. Seuraavissa vianmääritysvaiheissa käydään läpi mahdolliset pääsyyt.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Varmista, että asynkroniseen tilaukseen liittyvä tapahtuma on mennyt headquartersiin

Sähköisen kaupankäynnin tapauksessa mene headquartersin kohtaan **Vähittäismyynti ja kauppa \> Kyselyt ja raportit \> Verkkokaupan tapahtumat**. Jos sinulla on tilauksen vahvistusnumero, suodata tapahtumat syöttämällä vahvistusnumero **Kanavan viitetunnus** -kenttään. Jos sinulla ei ole vahvistusnumeroa, suodata tapahtumat syöttämällä asiakkaan tilinumero.

Myyntipistetilauksen tapauksessa avaa **Myymälän tapahtumat** -sivu ja suodata tietueet kuitin numeron tai asiakkaan tilinumeron mukaan. Jos tapahtumaa ei löydy, suorita kanavan tapahtumatyö **P-0001**, joka synkronoi tapahtumat kanavilta headquartersiin. Jos **P-0001**-työ epäonnistuu, avaa tukipalvelupyyntö työn epäonnistumisesta. Jos **P-0001**-työ onnistuu, mutta tapahtumat eivät silti näy headquartersissa, avaa tukipalvelupyyntö, joka sisältää tarvittavat tiedot.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Tarkista synkronoinnin tila, jos tapahtuma on olemassa headquartersissa, mutta sitä ei ole linkitetty myyntitilaukseen

Jos tapahtuma on olemassa headquartersissa, mutta myyntitilausta ei ole luotu, avaa **Verkkokaupan tapahtumat** -sivu ja valitse **Synkronoinnin tila** -pikavälilehti. Jos **Synkronoi tilaukset** -työ yritti synkronoida tämän tapahtuman, **Odottavan tilauksen tila** -kentässä tulisi olla tila **Onnistui** tai **Epäonnistui**. Jos tila on **Onnistui**, myyntitilauskentän on oltava tässä tapahtumassa. Jos tila on **Epäonnistui**, voit tarkastella virheen tietoja **Tilausvirheen tiedot** -kentässä **Synkronoinnin tila** -pikavälilehdellä. Jos kumpikaan näistä tiloista ei ole näkyvissä, tapahtumaa ei ole yritetty käsitellä. Tässä tapauksessa voit valita kohdan **Synkronoi tilaus** sivun yläosassa synkronointityön suorittamiseksi.

Varmista, että **Synkronoi tilaukset** -työ on ajoitettu suoritettavaksi kausittain, jotta asynkroniset tapahtumat voidaan luoda tilauksina headquartersissa.

Seuraavissa osissa on tietoja yleisistä virheistä ja niiden suositelluista korjauksista.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Tilausvirheen tiedot -kentässä näkyy seuraava virhesanoma: "Numerosarja on ylitetty"

Numerosarjoja käytetään myyntitilausten luomiseen headquartersissa. Jos kaikki numerosarjalle sallitut numerot on käytetty, järjestelmä luo tämän virhesanoman. Myyntitilausten luomiseen käytettävä numerosarja löytyy kohdasta **Myyntireskontran parametrit \> Numerosarjat \> Myyntitilaus**. Voit korjata tämän virheen korjaamalla aiemmin luodun numerosarjan tai korvaamalla sen uudella numerosarjalla.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Tilausvirheen tietokenttä näyttää seuraavan virhesanoman: "Luottokorttitapahtumien käsittelemiseksi on oltava oletusmaksupalvelu"

Voit korjata virheen vahvistamalla, että oletusmaksu on määritetty headquartersissa. Jos oletusmaksua ei ole määritetty, se on määritettävä. Siirry kohtaan **Myyntireskontra \> Maksun asetukset \> Maksupalvelut** ja varmista, että **Uusien luottokorttien oletuskäsittelijä** -vaihtoehdon arvo on **Kyllä** yhdelle maksupalvelulle.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Tilausvirheen tietokenttä näyttää tilirakenteen virhesanoman

Tilirakenteen virhesanoman teksti voi vaihdella, kuten seuraavissa esimerkeissä näkyy. Virheistä ilmenee kuitenkin yhteinen pääsyy, joka liittyy tilirakenteen konfiguraatioon.

- ”Kirjauskansion eränumeron 0009656328 Tosite ARP-000959899 1.00 tulokset kirjataan yrityksessä usrt liikamaksuksi tai alimaksuksi”
- "Kirjauskansion eränumeron 0009656328 Tosite ARP-000959899 Tosite ARP-000959901 tuloksia kirjataan Yhdistelmän 618160 tilirakenne ei kelpaa kirjanpidolle Yrityksen päätili jaettu"
- ”Kirjauskansion eränumero 0009656328 Tosite ARP-000959899 Tosite ARP-000959901 kirjauksen tulokset raportoitu yrityksen usrt tileiltä”
- ”Kirjauskansion eränumeron 0009656328 Tosite ARP-000959899 tuloksia kirjataan Kirjaus on peruutettu”
    
Voit korjata nämä virheet tarkistamalla tilirakenteet. Lisätietoja on ohjeaiheessa [Tilirakenteen määrittäminen](/dynamics365/finance/general-ledger/configure-account-structures).
    
Kun virhe on korjattu, valitse epäonnistunut tapahtuma ja valitse sitten sivun yläosassa **Synkronoi tilaus** synkronointityön suorittamiseksi.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Muuntyyppiset virheet, jotka saattavat edellyttää tapahtumatietojen korjaamista

Korjataksesi muuntyyppiset virheet, jotka saattavat edellyttää tapahtumatietojen korjaamista, voit käytää "tapahtumien muokkaaminen ja valvominen" -ominaisuutta. Lisätietoja: [Tapahtumien muokkaaminen ja valvominen](../edit-order-trans.md).
