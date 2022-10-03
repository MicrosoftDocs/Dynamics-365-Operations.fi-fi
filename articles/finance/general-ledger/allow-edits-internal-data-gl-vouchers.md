---
title: Salli sisäisten tietojen muokkaus kirjanpitotositteissa
description: Tässä artikkelissa on tietoja kirjanpitotositteiden sisäisten tietojen muokkaamista varten.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573248"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Salli sisäisten tietojen muokkaus kirjanpitotositteissa

[!include[banner](../includes/banner.md)]


Kun kirjaat kirjanpidon kirjauksia kirjanpitoon, **Kuvaus**-kenttää käytetään usein sisäisten huomautusten tai asiakirjojen tallentamista varten. Jos tiedot ovat virheelliset, se voi aiheuttaa sekaannusta ja vaikeuttaa kausien sulkemista. Tämän ominaisuuden avulla laskentapäällikkö tai taloushallintopäällikkö voi korjata virheitä muokkaamalla kirjanpitoon kirjattujen tositteiden **Kuvaus**-kenttää.

Kirjanpitoon kirjattujen tositteiden muutokset rajoittuvat sisäisiin tietoihin. Tämän toiminnon avulla ei koskaan voi muokata tietoja, kuten summia, kirjauspäivämääriä, kirjanpitotilejä ja tapahtuman valuuttaa. Muutokset tietoihin vaikuttavat raporttien ulkoiseen raportointiin, ja muutokset on tehtävä vain uusien kirjanpitotositteiden avulla.

> [!NOTE]
> Dynamics 365 Financen versiossa 10.0.29 tämä ominaisuus on saatavana vain **Kuvaus**-kentän muokkauksissa.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Muokkaa sisäisiä tietoja kirjanpitotositteissa

Ennen kuin kirjanpidon tositteiden sisäisiä tietoja voi muokata, **Salli sisäisten tietojen muokkaus kirjanpitotositteissa** -ominaisuus on otettava käyttöön **Ominaisuuksien hallinta** -työtilassa.
Kun ominaisuus on otettu käyttöön, kirjattuja tositteita muokkaavalle käyttäjälle on annettava laskentapäällikön tai taloushallintopäällikön rooli. Voit lisätä käyttöoikeuksia myös muihin rooleihin mukauttamalla käyttöoikeusrooleja.

Muokkausprosessi on sallittu vain Tositetapahtumat-sivulla.

1. Siirry kohtaan **Kirjanpito** > **Kyselyt ja raportit** > **Tositetapahtumat**.
2. Kirjoita **SysQuery**-valintaikkunaan tositteiden valintaa koskevat hakuehdot.
3. Valitse muokattavien tositteiden rivit ja valitse sitten **Muokkaa tositetta** > **Muokkaa sisäisiä tositetietoja**.

    [![Tositteen tapahtumat -sivu.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
**Muokkaa sisäisiä tositetietoja** -sivulla näkyvät seuraavat tiedot kullakin valitsemallasi rivillä:
  
  - Kirjanpitotili
  - Tilin nimi
  - Tosite
  - Nykyinen kuvaus
  - Uusi kuvaus

    [![Kirjaustosite.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Vain **Uusi kuvaus** -kenttää voi muokata. Oletusarvon mukaan arvo vastaa **Nykyinen kuvaus** -kentän arvoa, jotta voit nopeasti korjata kuvauksen pieniä virheitä.

4. Muokkaa kunkin rivin **Uusi kuvaus** -kenttää tai poista kuvaus kullakin rivillä.

   Vaihtoehtoisesti jos useita rivejä on päivitettävä samalla arvolla, noudata seuraavia ohjeita:

      1. Valitse muokattavat rivit ja valitse sitten **Päivitä valitut tietueet joukkotoimintona**.
      2. Valitse muokattava kenttä **Muokattava kenttä** -kentästä. Tällä hetkellä haku sisältää vain **Uusi kuvaus** -kentän.
      3. Syötä uusi kuvaus **Uusi arvo** -kentässä.
      4. Valitse **Päivitä**. Kaikille valituille tietueille päivitetään uusi arvo.

      [![Päivitä valitut tietueet joukkotoimintona -valintaruutu.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. Kirjoita **Muokkauksen syy** -kenttään huomautus, joka selittää muokkauksen syyn. Tämä huomautus näkyy kirjausketjun **Tositteiden muokkausten kirjausketju** -sivulla.

   Samaan tositteeseen voidaan tehdä useita muokkauksia, ja kutakin muokkausta seurataan.

## <a name="audit-trail-of-voucher-edits"></a>Tositteiden muokkausten kirjausketju

Kirjausketjua ylläpidetään erityisesti tämän ominaisuuden avulla tehtyjen muutosten seuraamiseen. Voit käyttää tositteen muokkauksen kirjausketjua kahdella tavalla:

  - Siirry kohtaan **Kirjanpito** > **Kyselyt ja raportit** > **Tositetapahtumat**. Valitse **Tositekyselyt**-sivulla **Muokkaa tositetta** > **Tositteiden muokkausten kirjausketju**. Kirjausketju näkyy vain valitun tositetietueen yhteydessä. 
   
    Avaamalla kyselyn tällä tavalla voit keskittyä kaikkiin yhteen tositetietueeseen tehtyihin muokkauksiin.
  
  - Valitse **Kirjanpito** > **Kausittaiset tehtävät** > **Tositteiden muokkausten kirjausketju**. Kirjoita valintaikkunaan ehdot, joiden mukaan voit määrittää tositteet, joiden muokkausten kirjausketjua haluat tarkastella. Jos haluat tarkastella kaikkien tositteiden kirjausketjua, jätä ehdot tyhjiksi ja valitse **OK**. 
    
    Kun avaat kyselyn tällä tavalla, voit suodattaa tietyn päivän tai tietyn käyttäjän tekemät muutokset.

**Muokkausten kirjausketju** -sivulla näkyvät seuraavat tiedot:

- **Luonnin päivämäärä ja aika** – Muokkauksen päivämäärä ja kellonaika.
- **Muokkauksen syy** – Syy, jonka käyttäjä on kirjoittanut muokkausta varten.
- **Luonut** – Muokkauksen tehnyt käyttäjä.

Voit tarkastella kunkin kirjausketjun tietoja porautumalla **Luonnin päivämäärä ja aika** -arvoon. **Näytä tositteen muokatut ominaisuudet** -sivulla näkyvät samat tiedot kuin alkuperäisellä muokkaussivulla, kuten aiempi kuvaus ja päivitetty kuvaus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
