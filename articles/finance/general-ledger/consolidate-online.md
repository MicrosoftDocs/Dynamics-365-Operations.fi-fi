---
title: Verkossa tapahtuma taloushallinnon konsolidointi
description: Tässä ohjeaiheessa käsitellään verkossa tapahtuvia taloushallinnon konsolidointeja kirjanpidossa.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 8a946a8325afebf76639991c60135d7425f5f211
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826759"
---
# <a name="online-financial-consolidations"></a>Verkossa tapahtuma taloushallinnon konsolidointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään verkossa tapahtuvia taloushallinnon konsolidointeja kirjanpidossa. Lue ennen tämän ohjeaiheen lukemista [Taloushallinnon konsolidointien ja valuutan muunnon yleiskatsaus](financial-consolidations-currency-translation.md).

Kun olet määrittänyt asetukset, anna konsolidointitiedot **Konsolidoi [Online]** -sivulla. Kun olet valmis käsittele konsolidointi valitsemalla **OK** tai **Erä**.

## <a name="criteria"></a>Kriteeri
Määritä **Konsolidoi [Online]** -sivun **Kriteeri**-välilehdessä tilit, kaudet ja konsolidoitavien tietojen tyyppi.

![Ehdot-välilehti](./media/criteria-consolidate-online.png "Ehdot-välilehti")

Välilehdessä olevien kenttien selitys:

- **Kuvaus** – anna konsolidoitavan kauden tarkka kuvaus.
- **Päätili** – määritä käsiteltävät päätilit tämän osan kentissä.

    - **Alkaen** ja **Asti** – Käsiteltävä tilialue. Jos jätät nämä kentät tyhjiksi, kaikkien yritysten kaikki tilit siirretään konsolidointiyritykseen. Niinpä jos konsolidoit neljä yritystä ja kullakin yrityksellä on eri tillikatta, kaikki neljän yrityksen tilit luodaan konsolidointiyrityksessä.
    - **Käytä konsolidointitiliä** – Jos valitset tässä **Kyllä**, **Valitse konsolidointitili seuraavasta** -kenttä on käytettävissä. Valitse tässä kentässä, konsolidoidaanko kaikki tilit **Päätilit**-sivulla määritetylle konsolidointitilille vai haluatko valita tilin jostakin konsolidointitiliryhmästä.
    - **Konsolidointitiliryhmä** – valitse ryhmä, jolla päätili yhdistetään konsolidoinnissa.

- **Konsolidointikausi** – määritä konsolidointikausi tässä osassa olevien kenttien avulla.

    - **Alkaen** ja **Asti** – Määritä konsolidoinnin päivämääräalue. Jos jätät nämä kentät tyhjiksi, konsolidointi käsitellään kaikilla yrityksen kirjanpidon kalenterissa määritetyillä kausilla. Näiden kenttien jättäminen tyhjäksi ei ole suositeltavaa.
    - **Sisällytä todelliset summat** – valitse **Kyllä**, jos haluat konsolidoida toteutuneet tiedot.
    - **Sisällytä budjettisummat**– valitse **Kyllä**, jos haluat konsolidoida budjettitiedot.
    - **Muodosta saldot uudelleen konsolidointiprosessin aikana** – Ei ole suositeltavaa, että asetuksessa valitaan **Kyllä**. Muodosta saldot sen sijaan uudelleen erillisenä erätyönä.

- **Budjettimallit** – jos olet valinnut budjettitietojen konsolidoinnin, määritä budjettimallit tämän osan kenttien avulla.

    - **Alkaen** ja **Asti** – määritä käytettävä mallialue.
    - **Budjettikurssin tyyppi** – valitse budjettitietojen valuuttamuunnossa käytettävän budjettikurssin tyyppi.

## <a name="financial-dimensions"></a>Taloushallinnon dimensiot
Määritä **Taloushallinnon dimensiot** -välilehdessä konsolidointiyritykseen sisällytettävät dimensiot. Valitse dimensio valitsemalla **Määritys**-kentässä **Dimensio** ja määrittämällä sitten konsolidointiyrityksen dimensiojärjestys.

![Taloushallinnon dimensiot -välilehti](./media/financial-dimensions-cons.png "Taloushallinnon dimensiot -välilehti")

Määritetystä järjestyksestä riippumatta, **Päätili** on aina ensimmäinen segmentti.

## <a name="legal-entities"></a>Oikeushenkilöt
Määritä **Oikeushenkilöt**-välilehdessä konsolidointiyritykseen sisällytettävät yritykset. Voit määrittää kyseisten yritysten omistajuusosuudet. Jos määritetty omistajuus on alle 100 prosenttia, määritetty prosenttiosuus kootaan konsolidointiyritykseen. **Muunnoserotusten tililaji** -kentässä valitaan mahdollisten muuntoerotusten yhteydessä päätili **Automaattisten tapahtumien tilit** -tilin asetuksista.

![Yritykset-välilehti](./media/legal-entities-cons.png "Yritykset-välilehti")

![Automaattisten tapahtumien tilit -sivu](./media/accounts-for-automatic-cons.png "Automaattisten tapahtumien tilit -sivu")

## <a name="elimination"></a>Eliminointi
**Eliminointi**-välilehdessä on kolme eliminointien käsittelyvaihtoehtoa:

- Valitse ensin eliminointisääntö ja sitten **Ehdotuksen asetukset** -kentässä **Vain ehdotus**. Tämä vaihtoehto käsittelee eliminoinnin konsolidointiprosessin aikana, mutta sitä ei kirjaa kaikkea yhtenä vaiheena. Voit kirjata kirjauskansion myöhemmin.
- Valitse ensin eliminointisääntö ja sitten **Ehdotuksen asetukset** -kentässä **Vain kirjaus**. Tämä vaihtoehto käsittelee eliminoinnin konsolidointiprosessin aikana ja kirjaa kaiken yhtenä vaiheena.
- Suorita eliminointiehdotus erillään konsolidointiprosessista käyttämällä eliminointikirjauskansiota.

![Eliminointi-välilehti](./media/elimination-cons-onl.png "Eliminointi-välilehti")

Lisätietoja eliminoinnista on kohdassa [Eliminointisäännöt](./elimination-rules.md).

## <a name="currency-translation"></a>Valuutan muuntaminen
**Valuutan muuntaminen** -välilehdessä määritetään yritys, tili, vaihtokurssi ja kurssi. **Käytä vaihtokurssia kohteesta** -kentässä on kolme vaihtoehtoa:

- **Konsolidointipäivämäärä** – Vaihtokurssi haetaan konsolidoinnin päivämäärän mukaan. Tämä kurssi vastaa spot-kurssia tai kuukauden lopussa voimassa olevaa kurssia. Näet kurssin esikatselun, mutta sitä ei voi muokata.
- **Tapahtumapäivä** – Vaihtokurssi valitaan kunkin tapahtuman päivämäärän perusteella. Tämä vaihtoehtoa käytetään useimmiten käyttöomaisuuden kanssa ja sitä kutsutaan usein historialliseksi kurssiksi. Kurssin esikatselu ei ole näkyvissä, koska tilialueella on useita erilaisten tapahtumien kursseja.
- **Käyttäjän määrittämä hinta** – Tässä vaihtoehdossa voit antaa haluamasi vaihtokurssin. Tämä vaihtoehto voi olla kätevä keskimääräisille vaihtokursseille tai silloin, kun konsolidoinnissa on käytössä kiinteä vaihtokurssi.

![Valuutan muuntotyyppi -välilehti](./media/currency-translation-cons-online.png "Valuutan muuntotyyppi -välilehti")

## <a name="additional-resources"></a>Lisäresurssit

Lisätietoja konsolidoinnista ja valuutan muuntamisesta on tämän ohjeaiheen pääaiheessa [Taloushallinnon konsolidointien ja valuutan muunnon yleiskatsaus](./financial-consolidations-currency-translation.md).

Lisätietoja skenaarioista, joissa voidaan laatia konsolidoituja raportteja, on kohdassa [Konsolidoitujen raporttien laatiminen](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]