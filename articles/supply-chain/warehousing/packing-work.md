---
title: Lähtevien konttien pakkaaminen ja toimitusten käsittely
description: Tässä artikkelissa kuvataan "Pakkaus"-työtilaustyyppi, joka hallitsee konttien pakkaustöitä. Se tukee myös osittaisia lähetyksiä pakatuille konteille, jotka on liitetty pakkaamattomia varastonimikkeitä sisältäviin kuormiin.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220549"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Lähtevien konttien pakkaaminen ja toimitusten käsittely

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan *Pakkaus*-työtilaustyyppi, joka hallitsee konttien pakkaustöitä. Se tukee myös osittaisia lähetyksiä pakatuille konteille, jotka on liitetty pakkaamattomia varastonimikkeitä sisältäviin kuormiin. Pakkaustöiden avulla voit käyttää [vahvistus- ja siirto-ominaisuuksia](confirm-and-transfer.md) vahvistaaksesi lähteviä lähetyksiä, jotka on liitetty kontteihin.

Pakkaustyö luodaan automaattisesti, kun lähdeasiakirjan työhön liittyvä varasto asetetaan *Pakkaussijainti*-tyyppiseen sijaintiin. Työ koostuu kahdesta rivistä, *Nouto* ja *Määritä*, ja sitä ylläpidetään automaattisesti osana konttien sulkemis-/uudelleenavaamisprosessia.

Lisätietoja konttien pakkausprosessin määrittämisestä ja käytöstä on kohdassa [Lähetettävien konttien pakkaaminen](packing-containers.md).

## <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Jos järjestelmäsi ei vielä sisällä tässä artikkelissa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota seuraavat ominaisuudet käyttöön seuraavassa järjestyksessä. Molemmat ominaisuudet sisältyvät **Varastonhallinta**-moduuliin.

1. *Vahvistus ja siirtäminen*
1. *Pakkausasemien pakkaustyö*

## <a name="set-up-a-location-for-packing-work"></a>Sijainnin määrittäminen pakkaustyötä varten

Määritä paikannussijainteja noudattamalla seuraavia ohjeita. Voit valita kullekin sijainnille, luoko järjestelmä pakkaustyön automaattisesti.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausaseman määritys**.
1. Lisää pakkausaseman määritystietue valitsemalla toimintoruudusta **Uusi**.
1. Määritä uudessa tietueessa seuraavat kentät:

    - **Varasto** – Valitse tai syötä varasto, jossa pakkaussijainti sijaitsee.
    - **Sijainti** – Valitse tai syötä pakkaussijainti. Tämä sijainti täytyy kohdistaa sijaintiprofiilille, joiden käyttämä sijaintityyppi on määritetty yrityksesi pakkaussijaintityypiksi **Varastonhallinnan parametrit** -sivulla. Lisätietoja on kohdassa [Lähetettävien konttien pakkaaminen](packing-containers.md).
    - **Luo pakkaustyö** – Valitse tämä valintaruutu luodaksesi pakkaustyön joka kerta, kun pakkaussijaintiin toimitetaan nimikkeitä. Työ sisältää linkit sen kuormariveihin, jotta osittaisia kuormia voidaan pakata ja lähettää.

## <a name="example-scenario"></a>Esimerkkiskenaario

Tässä esimerkissä kuvataan, miten lähtevien myyntitilausten työnkulku käsitellään pakkaamalla kontti ja lähettämällä osittainen kuorma.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit käyttää tätä skenaariota ohjeena ominaisuuden käyttämiseen tuotantojärjestelmässä. Siinä tapauksessa tässä kuvatut arvot on kuitenkin korvattava omilla arvoilla.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Pakkaustyön määrittäminen varaston pakkaussijainnille

Sinun täytyy määrittää *Pakkaus*-työprosessi tietylle varastolle ja sijainnille päästäksesi alkuun.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausaseman määritys**.
1. Lisää uusi määritystietue valitsemalla toimintoruudusta **Uusi**.
1. Aseta uudelle tietueelle seuraavat arvot:

    - **Varasto**: *62*
    - **Sijainti:** *Pakkaus*
    - **Luo pakkaustyö:** *Kyllä*

1. Sulje **Pakkausaseman määritys** -sivu.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Osittaisen lähetyksen sallivan kuormamallin luominen

Jos haluat sallia kuorman toimituksen useissa lähetyksissä, sinun täytyy liittää se kuormamalliin, joka sallii osittaisen lähetyksen. Luo tarvittava malli noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Kuorma \> Kuormamallit**.
1. Lisää uusi määritystietue valitsemalla toimintoruudusta **Uusi**.
1. Aseta uudelle tietueelle seuraavat arvot:

    - **Kuorman mallitunnus:** *Osittainen*
    - **Salli kuormituksen jakaminen lähetyksen vahvistuksen aikana:** *Kyllä*

1. Sulje **Kuormituksen mallit** -sivu.

Lisätietoja on kohdassa [Vahvistus ja siirtäminen](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Myyntitilauksen käsittely

Voit käsitellä myyntitilauksen ja lähettää sen osittain noudattamalla seuraavia ohjeita.

1. Suorita [Lähetettävien konttien pakkaaminen](packing-containers.md) -osiossa kuvattu [esimerkkiskenaario](packing-containers.md#scenario). Tämän skenaarion aikana luot myyntitilauksen yhden nimikkeen kahdelle osalle. Tämän jälkeen pakkaat vain toisen näistä osista konttiin ja suljet kontin. Sinun tulisi kirjoittaa luomasi lähetyksen tunnus muistiin skenaarion ohjeiden mukaisesti.
1. Valitse **Varastonhallinta \> Työ\> Kaikki työt**.
1. Valitse suodatinalueelta **Näytä suljettu työ** -valintaruutu. Syötä sitten lähetyksen tunnus **Suodatin**-kenttään ja valitse suodatusehdoksi **Lähetyksen tunnus** -arvo. Sinun pitäisi nähdä nyt kolme työotsikkoa. Yksi on myyntitilauksen keräystyö, ja sen tila on *Suljettu*. Kaksi on pakkausprosessille: toinen liittyy suljettuun konttiin, ja sen tila on *Suljettu*, ja toinen liittyy vielä pakkaamattomaan nimikkeeseen, ja sen tila on *Avoin*.
1. Valitse **Kuormituksen tunnus** -arvo mille tahansa työotsikolle avataksesi kuorman **Kuorman tiedot** -sivun.
1. Vaihda **Otsikko**-näkymään.
1. Valitse **Yleiset**-pikavälilehdestä **Kuorman mallitunnus** -kentän **Muokkaa**-painike. Valitse sitten tätä skenaariota varten luomasi osittaisen lähetyksen kuormamalli (*Osittainen*).
1. Valitse toimintoruudun **Lähetä ja vastaanota** -välilehden **Vahvista**-ryhmässä **Lähtevä lähetys**.
1. Valitse **Lähetyksen vahvistus** -valintaikkunasta **Jaa määrä uuteen kuormitukseen** -vaihtoehto.
1. Valitse **OK**.

Olet nyt lähettänyt yhden alkuperäiseen kuormaan liittyvän kontin, ja järjestelmä on luonut uuden kuorman jäljellä oleville nimikkeille, jotka täytyy vielä pakata kontteihin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
