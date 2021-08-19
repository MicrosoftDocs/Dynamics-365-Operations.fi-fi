---
title: Indeksikorkoon linkitettyjen vuokrien uudelleenarvostus
description: Tässä ohjeaiheessa kuvataan oikaisu, joka tehdään käyttöoikeusomaisuuserän velan vuokraamista varten, kun muuttuvat vuokrat muuttuvat indeksikoron muuttumisen vuoksi.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1b3eed28ba6fc5af02c1bbf430cc9779426084f0eaf4e027141bbdd18a70dde4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734583"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Indeksikorkoon linkitettyjen vuokrien uudelleenarvostus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan oikaisu, joka tehdään käyttöoikeusomaisuuserän velan vuokraamista varten, kun muuttuvat vuokrat muuttuvat indeksikoron muuttumisen vuoksi. Vuokravelka ja käyttöoikeusomaisuuserä oikaistaan tilille uusia maksusummia varten. ASC 842 -standardin (joka on Yhdysvaltojen yleisti hyväksytty kirjanpitostardardi US GAAPI) mukaan vain muuttuvat maksut muuttuvat, kun maksuja lisätään tai vähennetään indeksikoron muuttumisen vuoksi, ellei kassavirroissa ole muita muutoksia. Näitä lisämuutoksia voivat olla korkoprosentteihin liittyvät vuokra-aikojen muutokset. Lisätietoja on ASC 842-10-55-225 -asiakirjassa ja IFRS 16:n kappaleessa 42(b).

## <a name="adjust-lease-payments"></a>Vuokrien muokkaaminen

Näiden vaiheiden avulla voit arvostaa uudelleen indeksikorkoon linkitetyt vuokrat.

1. Voit suorittaa vuokrasopimuksen indeksin uudelleenarvostusprosessin siirtymällä kohtaan **Resurssin vuokraus \> Kausittainen \> Indeksikoron uuudelleenarvostus**.

    **Indeksikoron uudelleenarvostus** -sivu tulee esille. Se sisältää kaikki edelliset suoritetut vuokrasopimuksen indeksin uudelleenarvostusprosessit. Tämän sivun tiedot sisältävät prosessin tunnuksen, joka luotiin numerojärjestyksen asetuksesta, yrityksen, oikaistujen vuokrauskirjojen määrän, velan oikaisun kokonaismäärän IFRS 16 -vuokrauksia varten ja ASC 842 -vuokrauksia varten oikaistujen muuttuvien maksujen kokonaismäärän.

2. Voit suorittaa uudelleenarvostuksen valitsemalla toimintoruudussa **Vuokrasopimuksen indeksin uudelleenarvostus**.

    **Indeksin uudelleenarvostuksen parametrit** -valintaikkuna tulee näkyviin. Tässä voit suodattaa ja valita vuokrasopimukset, vuokrausryhmät ja muut ehdot, joiden mukaan uudelleenarvostettavat vuokraukset valitaan. Lisäksi **Suorita taustalla** -välilehdessä voit määrittää indeksin uudelleenarvostusprosessin niin, että se suoritetaan eränä.

4. Valitse suodattimet taustaprosessiin sisällytettävien vuokrasopimusten valintaa varten ja valitse sitten **OK**.

    Näyttöön tulee **Indeksikoron uudelleenarvostuksen esikatselu** -valintaikkuna, jossa näkyvät uudelleenarvostettavat vuokrasopimukset. Se näyttää myös resurssin ja velan oikaisut tai muuttuvien maksujen oikaisut.
    
5. Jos haluat estää vuokrasopimusten uudelleenarvostuksen, valitse vuokrasopimukset, jotka **tulee** arvostaa uudelleen. Jos et valitse vuokrasopimuksia, kaikki vuokrasopimukset arvostetaan uudelleen. Kun olet valmis, arvosta vuokrat uudelleen valitsemalla **OK**.
6. Jos haluat tarkastella tietylle indeksin uudelleenarvostusprosessille luotuja tapahtumia, valitse prosessitunnus ja valitse sitten **Tapahtumat**.

    Näyttöön tulee valintaikkuna, joka sisältää käsittelyn aikana luotujen tapahtumien tiedot.

> [!NOTE]
> Vain sellaiset vuokrasopimukset, joiden uudelleenarvostuspäivämäärä on järjestelmän päivämäärä tai aikaisempi, voidaan arvostaa uudelleen. Järjestelmä ohittaa automaattisesti kaikki vuokrasopimukset, joiden uudelleenarvostuspäivämäärä on myöhempi kuin järjestelmän päivämäärä.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 -vuokraukset – indeksin uuudelleenarvostus

Jos haluat tarkastella vuokrausten uudelleenarvostusprosessin vaikutusta ASC 842 -vuokrauksiin, avaa vuokrauksen maksuaikataulu. Sivulla ovat vain muuttuvat maksut, jotka on tehty sen jälkeen, kun uudelleenarvostuspäivämäärää muutettiin indeksin uudelleenarvostuksen vuoksi, tai kyseisenä päivänä. Kuoletus- ja poistoaikatauluja ei muuteta. Kun luot laskun, jolla on muuttuva maksu, muuttuva maksu veloitetaan muuttuvan maksun kirjaustililtä. Myös muuttuvan maksun summa lisätään hyvitysvientiin, joka kirjattiin suoraan toimittajalle tai velkavekselitilille vuokrauskirjan asetuksen mukaan.

Vuokrauksen tietojen sivun maksuaikataulurivit päivitetään automaattisesrti uuden indeksiprosentin sisältävän rivin avulla. Lisäksi sarakkeessa näkyy, onko rivi luotu manuaalisesti vai indeksin uudelleenarvostusprosessin kautta.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 -vuokraukset – indeksin uuudelleenarvostus

Jos haluat tarkastella vuokrausten uudelleenarvostusprosessin vaikutusta IFRS 16 -vuokrauksiin, avaa oikaistun vuokrauksen tiedot. **Vuokra-aika**- ja **Resurssin käyttöikä** -kentät on päivitetty niin, että ne näyttävät ajan alkamispäivämäärästä tai muokkauspäivämäärästä lähtien uudelleenarvostuspäivämäärään asti. Lisäksi maksuaikataulurivit on päivitetty niin, että ne muuttuvat vuokrauksen uusien maksujen, uuden indeksikoron ja rivin luontitavan mukaisesti.

Voit tarkastella vain juuri luotua maksuaikataulua, joka alkaa uudelleenarvostuspäivämäärästä ja näyttää päivitetyn maksusumman kokonaismäärän. Myös uusi vuokrasopimusvelan kuoletusaikatauku ja resurssin poistoaikataulu on luotu. Ne muuttavat oikaistua maksuaikataulua.

Kirjauskansiovienti on kirjannut automaattisesti oikaisukirjauskansioviennin tilille niiden vuokrien muutokselle, jotka liittyvät indeksin uudelleenarvostukseen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
