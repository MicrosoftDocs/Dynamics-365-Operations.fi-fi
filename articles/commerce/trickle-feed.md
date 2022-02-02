---
title: Vähittäismyyntitapahtumien vähittäisiin syötteisiin perustuvien tilausten luominen
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commerce -sovelluksen tapahtumien syötteisiin perustuvien tilausten vähittäisestä luomisesta.
author: analpert
ms.date: 01/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964626"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Vähittäismyyntitapahtumien vähittäisiin syötteisiin perustuvien tilausten luominen

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commercen versiossa 10.0.5 ja uudemmissa versioissa suositellaan siirtämään kaikkien laskelmien kirjausprosessit vähittäisiin syötteisiin perustuviksi laskelmien kirjausprosesseiksi. Vähittäisten syötteiden toimintoon liittyy merkittäviä suorituskyvyn ja liiketoiminnan etuja. Myyntitapahtumia käsitellään koko päivän ajan. Maksuvälineiden ja kassanhallinnan tapahtumat käsitellään tapahtumaraportissa päivän lopuksi. Vähittäisten syötteiden toiminto mahdollistaa myyntitilausten, laskujen ja maksujen jatkuvan käsittelyn. Tämän vuoksi varasto, tuotto ja maksut päivitetään ja kirjataan lähes reaaliaikaisesti.

## <a name="use-trickle-feed-based-posting"></a>Vähittäisiin syötteisiin perustuvien kirjausten käyttäminen

> [!IMPORTANT]
> Ennen kuin otat käyttöön vähittäisiin syötteisiin perustuvan kirjauksen, varmista, että laskemattomia ja kirjaamattomia laskelmia ei ole. Kirjaa kaikki laskelmat, ennen kuin otat toiminnon käyttöön. Voit tarkistaa avoimet laskelmat **Myymälän myyntitiedot** -työtilassa.

Jos haluat ottaa käyttöön vähittäiseen syöttöön perustuvan vähittäismyyntitapahtumien kirjaamisen, ota käyttöön **Vähittäismyyntilaskelmat - vähittäinen syöte** -toiminto **Ominaisuuksien hallinta** -työtilassa. Laskelmat jaetaan kahteen tyyppiin: tapahtumaraportit ja tilipäätökset.

### <a name="transactional-statements"></a>Tapahtumaraportit

Tapahtumaraporttien käsittely tulee suorittaa usein päivän aikana. Asiakirjat luodaan, kun tapahtumat ladataan Commerce-pääkonttorisovellukseen. Tapahtumat ladataan myymälöistä Commerce-pääkonttorisovellukseen, kun **noutotyö** suoritetaan. Suorita myös **Tarkista myymälän tapahtumat** -työ, jos haluat tarkistaa tapahtumat, jotka tapahtumaraportti valitsee.

Ajoita seuraavat usein suoritettavat työt:

- Jos haluat laskea tapahtumaraportin, suorita **Laske tapahtumaraportit eräajona** -työ (**Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus \> Laske tapahtumaraportit eräajona**). Tämä työ valitsee kaikki kirjaamattomat ja tarkistetut tapahtumat ja lisää ne uuteen tapahtumaraporttiin.
- Jos haluat kirjata tapahtumaraportit eräajona, suorita **Kirjaa tapahtumaraportit eräajona** -työ (**Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus \> Kirjaa tapahtumaraportit eräajona**). Tämä työ suorittaa kirjausprosessin ja luo myyntitilaukset, myyntilaskut, maksukirjauskansiot, alennuskirjauskansiot sekä tulo- ja kulutapahtumat kirjatuista laskelmista, joissa ei ole virheitä. 

### <a name="financial-statements"></a>Tilinpäätökset

Tilinpäätösten käsittelyprosessi on tarkoitettu suoritettavaksi päivän lopussa. Tämäntyyppinen tilinpäätösten käsittely tukee vain **Vuoro**-sulkemistapaa. Se valitsee vain suljetut vuorot. Tilinpäätökset koskevat vain taloushallinnon täsmäytystä. Tämä luo kirjauskansiot vain maksuvälineiden lasketun summan ja tapahtuman summan välisille eroaville summille ja muun kassanhallinnan tapahtumille.

Tilinpäätökset mahdollistavat myös seuraavien tapahtumien tarkastelun: kassan laskemistapahtumat maksuvälineittäin, maksutapahtumat, pankkiin toimitetut maksuvälinetapahtumat ja kassakaapin maksuvälinetapahtumat. Maksuvälineen tietosivu näkyy vain silloin, kun tilinpäätös on valittuna.

![Kuvassa näkyy kirjattujen laskelmien lomakkeen maksuvälineen tietosivu vain silloin, kun tilinpäätös on valittuna.](./media/Trickle-feed-posted-statements-transaction-view.png)

Ajoita seuraavien tilinpäätöstöiden aloitus- ja päättymisajat päivän odotetun päättymisen perusteella seuraavasti:

- Jos haluat laskea tilinpäätöksen, suorita **Laske tilinpäätökset eräajona** -työ (**Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus \> Laske tilinpäätökset eräajona**). Tämä työ kerää kaikki kirjaamattomat kirjanpitotapahtumat ja lisää ne uuteen tilinpäätökseen.
- Jos haluat kirjata tilinpäätökset eräajona, suorita **Kirjaa tilinpäätökset eräajona** -työ (**Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus \> Kirjaa tilinpäätökset eräajona**).

### <a name="manually-create-statements"></a>Laskelmien luominen manuaalisesti

Tapahtumaraportin ja tilinpäätöksen tyypit voidaan luoda myös manuaalisesti. 

1. Siirry kohtaan **Retail ja Commerce \> Kanavat \> Myymälät** ja valitse **Laskelmat**. 
2. Valitse **Uusi** ja valitse sitten luotavan laskelman tyyppi. **Laskelmat**-sivun kentissä on valittuun laskelmatyyppiin liittyviä tietoja. **Laskelmaryhmä**-kohdassa näkyvät liittyvät toiminnot.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
