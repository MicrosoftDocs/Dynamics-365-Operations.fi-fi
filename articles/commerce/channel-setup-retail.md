---
title: Vähittäismyyntikanavan määrittäminen
description: Tässä artikkelissa käsitellään uuden vähittäismyyntikanavan luomisesta Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eccbbff33ddf967b000940a8ea9910c34232431f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847729"
---
# <a name="set-up-a-retail-channel"></a>Vähittäismyyntikanavan määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään uuden vähittäismyyntikanavan luomisesta Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia. Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat). Jokaisella vähittäismyymäläkanavalla voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta. Sinun on määritettävä kaikki nämä elementit, ennen kuin voit luoda vähittäismyymäläkanavan. 

Varmista ennen vähittäismyyntikanavan luontia, että [kanavan edellytykset](channels-prerequisites.md) toteutuvat.

## <a name="create-and-configure-a-new-retail-channel"></a>Uuden vähittäismyyntikanavan luominen ja määrittäminen

1. Valitse siirtymisruudussa **Moduulit \> Kanavat \> Myymälät \> Kaikki myymälät**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Nimi**-kenttään uuden kanavan nimi.
1. Anna yksilöivä myymälän numero **Myymälän numero** -kenttään. Numero voi olla aakkosnumeerinen, ja siinä saa olla enintään 10 merkkiä.
1. Anna sopiva yritys avattavassa **Yritys**-luettelossa.
1. Anna sopiva varasto avattavassa **Varasto**-luettelossa.
1. Valitse sopiva aikavyöhyke **Myymälän aikavyöhyke** -kentässä.
1. Valitse myymälään sopiva arvonlisäveroryhmä avattavassa **Arvonlisäveroryhmä**-luettelossa.
1. Valitse sopiva valuutta **Valuutta**-kentässä.
1. Anna kelvollinen osoitekirja **Asiakkaan osoitekirja** -kentässä.
1. Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä.
1. Valitse toimintoprofiili tarvittaessa **Toimintoprofiili**-kentässä.
1. Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näytetään, miten uusi vähittäismyyntikanava luodaan.

![Uusi vähittäismyyntikanava.](media/channel-setup-retail-1.png)

Seuraavassa kuvassa on esimerkki vähittäismyyntikanavasta.

![Vähittäismyyntikanavan esimerkki.](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Muut asetukset

**Laskelma/sulkeminen**- ja **Muut**-osissa on monia määritettäviä valinnaisia asetuksia. Nämä määritykset voidaan tehdä vähittäismyymälän tarpeiden mukaan.

Lisätietoja näytön oletusasettelun määrittämisestä **Näytön asettelu** -osassa on kohdassa [Näytön asettelut myyntipisteeseen (POS)](pos-screen-layouts.md) ja **Laiteasema**-osan määritystiedoista on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](retail-hardware-station-configuration-installation.md).

Seuraavassa kuvassa on esimerkki vähittäismyyntikanavan asetusten määrityksistä.

![Vähittäismyyntikanavan määritysesimerkki.](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Lisäkanavan määrittäminen

Muita kanavaan määritettäviä kohteita on **Asetukset**-osan toimintoruudussa.

Verkkokanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen, kassatilityksen, toimitustapojen, tulo- ja kulutilin, osien, täytäntöönpanoryhmään määrityksen ja säilöjen määrittäminen.

Seuraavassa kuvassa on erilaisia vähittäismyyntikanavan määritysvaihtoehtoja **Asetukset**-välilehdessä.

![Kanavan määrittäminen.](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse maksutapa siirtymisruudussa.
1. Anna **Yleiset**-osassa **Toiminnon nimi** ja määritä muut mahdolliset asetukset.
1. Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.

![Esimerkki maksutavoista.](media/channel-setup-retail-5.png)

Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta ja **Summa**-välilehden konfiguraatiosta.

![Summien esimerkkimaksutavan asetukset.](media/payment-methods-recount.png)

> [!NOTE]
> **Summa**-välilehden arvot tallennetaan välimuistiin Retail Serverissa, eivätkä ne tule voimaan heti jakeluaikataulun töiden suorittamisen jälkeen. Voit ottaa nämä arvot välittömästi käyttöön testausta varten, kun käynnistät Cloud Scale Unitin uudelleen.

### <a name="set-up-cash-declaration"></a>Kassatilityksen määrittäminen

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Kassatilitys**.
1. Valitse toimintoruudussa **Uusi** ja luo sitten kaikki tarvittavat **Kolikko**- ja **Seteli**-arvot.

Seuraavassa kuvassa näkyy esimerkki kassatilityksestä.

![Kassatilitysten määrittäminen.](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Määritä toimitustavat

Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** toimintoruudun **Asetukset**-välilehdessä.  

Voit muuttaa toimitustapaa tai lisätä sen seuraavien ohjeiden mukaisesti.

1. Valitse siirtymisruudussa **Moduulit \> Varastonhallinta \> Toimitustavat**.
1. Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.
1. Lisää kanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**. Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.

Seuraavassa kuvassa on esimerkki toimitustavasta.

![Määritä toimitustavat.](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Tulo- ja kulutilin määrittäminen

Voit määrittää tulo- ja kulutilin noudattamalla seuraavia ohjeita.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Tulo- ja kulutili**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna nimi **Nimi**-kohdassa.
1. Anna hakunimi **Hakunimi**-kohdassa.
1. Anna tilityyppi **Tilityyppi**-kohdassa.
1. Kirjoita tarpeen mukaan tekstiä seuraaviin kohtiin: **Sanomarivi 1**, **Sanomarivi 2**, **Luetteloteksti 1** ja **Luetteloteksti 2**.
1. Anna kirjauksen tiedot **Kirjaus**-kohtaan.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa on esimerkki tulo- ja kulutilistä.

![Tulo- ja kulutilien määrittäminen.](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Osien määrittäminen

Voit määrittää osia noudattamalla seuraavia ohjeita.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Osat**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna osan numero **Osan numero** -kohtaan.
1. Anna kuvaus **Kuvaus**-kohtaan.
1. Anna osan koko **Osan koko** -kohtaan.
1. Määritä tarpeen mukaan **Yleiset**- ja **Myyntitilastot**-asetukset.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Täytäntöönpanoryhmän määrityksen määrittäminen

Voit määrittää täytäntöönpanoryhmän määrityksen noudattamalla seuraavia ohjeita.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Täytäntöönpanoryhmän määritys**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse täytäntöönpanoryhmä avattavassa **Täytäntöönpanoryhmä**-luettelossa.
1. Anna kuvaus avattavassa **Kuvaus**-luettelossa.
1. Valitse toimintoruudussa **Tallenna**

Seuraavassa kuvassa on esimerkki täytäntöönpanoryhmän määrityksen määrittämisestä.

![Täytäntöönpanoryhmän määritysten määrittäminen.](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Säilöjen määrittäminen

Voit määrittää säilöjä noudattamalla seuraavia ohjeita.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Säilöt**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna säilön nimi.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="ensure-unique-transaction-ids"></a>Yksilöivien tapahtumatunnusten varmistaminen

Commerce-version 10.0.18 jälkeen myyntipistettä varten luodut tapahtumatunnukset ovat peräkkäisiä, ja ne sisältävät seuraavat osat:

- Kiinteä osa, joka on myymälän tunnuksen ja päätteen tunnuksen ketjutus. 
- Peräkkäinen osa, joka on numerosarja. 

Muoto on tarkalleen ottaen *{store}-{terminal}-{numbersequence}*. 

Koska tapahtumatunnuksia voi luoda offline-tilassa ja online-tiloissa, luotuja tapahtumatunnuksia on olemassa kaksoiskappaleita. Tapahtumatunnuksen kaksoiskappaleiden poistaminen edellyttää manuaalisten tietojen korjausta. 

Commerce-versiossa 10.0.19 tapahtumatunnuksen muoto on päivitetty poistamaan järjestysosa ja siinä käytetään sen sijaan 13-numeroista lukua, joka on luotu laskemalla aika millisekunteina 1970 jälkeen. Muutoksen jälkeen uusi tapahtumatunnuksen muoto on *{store}-{terminal}-{millisecondsSince1970}*. Tämä päivitys tekee tapahtumatunnuksesta ei-peräkkäisen ja varmistaa, että tapahtumatunnukset ovat aina yksilöiviä. 

> [!NOTE]
> Tapahtumatunnukset on tarkoitettu vain sisäistä järjestelmää varten, joten niiden ei tarvitse olla peräkkäisiä. Monissa maissa kuittitunnusten pitää kuitenkin olla peräkkäisiä.

Uuden tapahtumatunnuksen muoto-ominaisuuden voi ottaa käyttöön **Ominaisuuksien hallinta** -työtilassa. 

Voit ottaa uudet tapahtumatunnukset käyttöön seuraavasti:

1. Valitse Commerce-pääkonttorissa **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
1. Suodata "retail ja commerce" -moduuli.
1. Etsi **Ota käyttöön uusi tapahtumatunnus tapahtumatunnusten kaksoiskappaleiden estämiseksi** -toiminnon nimeä.
1. Valitse ominaisuus ja valitse sitten oikeanpuoleisesta ruudusta **Ota käyttöön nyt**.  
1. Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.
1. Suorita **1070 Kanavan määritys**- ja **1170 Myyntipisteen tehtävien tallennustoiminto** -työt synkronoidaksesi käyttöönotetut ominaisuudet myymälöihin.
1. Kun muutokset on lähetetty myymälöihin, myyntipistepäätteet on suljettava ja avattava uudelleen, jotta uutta tapahtumatunnuksen muotoa voi käyttää. 

> [!NOTE]
> Kun uuden tapahtumatunnuksen muoto-ominaisuus on käytössä, et voi poistaa toimintoa käytöstä. Jos se on poistettava käytöstä, ota yhteyttä Commerce-tukeen.

## <a name="additional-resources"></a>Lisäresurssit

[Kanavien yleiskatsaus](channels-overview.md)

[Kanavan määrittämisen edellytykset](channels-prerequisites.md)

[Verkkokanavan määrittäminen](channel-setup-online.md)

[Puhelinkeskuskanavan määrittäminen](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
