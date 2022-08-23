---
title: Julkaisuryhmien käsittely
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen julkaisuryhmät-ominaisuutta.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 5a19d25b0b34ea3d452cacdd51ea071747ff1d90
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279002"
---
# <a name="work-with-publish-groups"></a>Julkaisuryhmien käsittely

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen julkaisuryhmät-ominaisuutta.

Verkkokauppasivustoja päivitetään jatkuvasti uudella sisällöllä koko vuoden ajan. Päivitykset julkaistaan usein vilkkaissa verkkokaupan tapahtumissa, kuten juhlapäivinä, kausiluonteisissa markkinointikampanjoissa tai kampanjalanseerauksissa. Nämä päivitykset edellyttävät usein, että sivuston sisältöryhmiä (esimerkkejä, sivuja, kuvia, fragmentteja ja malleja) vaiheistetaan, validoidaan ja julkaistaan samanaikaisesti yhdessä toiminnassa.

Kyky ryhmitellä kohteita loogisiin joukkoihin, jotka julkaisevat nimikkeitä yhdessä, jossa kullakin joukoilla on oma elinkaarensa, tarjoaa monia etuja sivuston tekijöille. Kaupassa näitä loogisia joukkoja kutsutaan julkaisuryhmiksi. Niiden avulla sivuston tekijät voivat seurata päivitysten sarjaa omiin määritettävissä oleviin, testattavissa oleviin ja julkaistavissa oleviin entiteetteihin.

Tekijät voivat esikatsella vaiheittainen julkaisuryhmän päivityksiä vaikuttamatta päivittyvään sivustoon tai muihin itsenäisissä julkaisuryhmissä. Tämän jälkeen tekijät voivat ajoittaa Julkaise-toiminnon julkaisemaan samanaikaisesti kaikki julkaisuryhmän kohteet Live-sivustoon. Mahdollisuus ryhmitellä, esikatsella ja ajoittaa julkaisemisen päivityksiä on tärkeää monille yritystason yrityksille, jotka tuottavat huomattavan vuosittaisen tuoton tapahtumapohjaisten sivustopäivitysten välitavoitteiden ympärille.

Yrityksille voi aiheutua kustannuksia hitaista tai mitätöidyistä sisällön käyttöönotoista, jotka eivät mene sujuvasti. Julkaise-ryhmät auttavat takaamaan, että lanseeraukset järjestetään, validoidaan ja julkaistaan ajoissa. Olivatpa ne suuria tai pieniä, julkaisuryhmät tarjoavat arvokkaan työkalujoukon, joka auttaa tekijöitä järjestämään ja yksinkertaistamaan meneillään olevia sivuston päivitystehtäviä.

## <a name="when-to-use-publish-groups"></a>Julkaisuryhmien käyttäminen

Voit käyttää julkaisuryhmiä aina, kun sinun on lakattava ja julkaistava useita asiakirjoja yhdessä. Jos sivustosi esimerkiksi päivittää sisältöä joka kausi, voit luoda julkaisuryhmiä näitä kausittaisia markkinointiliikkeitä varten. Syksyn kausipäivitys-julkaisuryhmä saattaa sisältää uusia kausittaisia kuvia, fragmentteja, joilla on kausittaisia markkinointiviestejä, vuodenajalle tyypillisiä tuotekokoelmia sisältäviä sivuja tai muita kausittaisia verkkosivustojen päivityksiä.

Julkaisuryhmien etuna on, että voit tehdä useita päivityksiä rinnakkain. Esimerkiksi pian syksyn kausipäivitys -julkaisuryhmän päivityksen jälkeen saattaa olla tietyn lomaviikonlopun sisältöpäivitys. Tässä tapauksessa voit julkaista syksyn kausiluonteinen päivitys -ryhmän sisällön samaan aikaan, kun lisäät seuraavan syksyn lomapäivityksen julkaisuryhmän sisältöä. Jokaisella julkaisuryhmällä on oma yksilöllinen sivu-, kuva-, fragmentti- ja mallijoukko. Voit lavastaa, esikatsella ja tarkistaa näitä kahta julkaisuryhmää itsenäisesti, mutta samanaikaisesti samalla aikajanalla. Jokainen julkaisuryhmä voidaan sitten ajoittaa julkaistavaksi sivustollasi tiettyinä päivinä ja kellonaikoina.

## <a name="turn-on-the-publish-groups-feature"></a>Julkaisuryhmät-toiminnon ottaminen käyttöön

Julkaisuryhmät-ominaisuus on valinnainen, ja se on otettava käyttöön sivustollasi.

Jos haluat ottaa julkaisuryhmät -ominaisuuden käyttöön sivustollasi Commerce -julkaisutyökaluissa, toimi seuraavasti.

1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.
1. Valitse **Sivuston asetukset** -kohdasta **Ominaisuudet**.
1. Määritä **Julkaisuryhmät**-asetukseksi **Käytössä**.

## <a name="create-a-publish-group"></a>Julkaisuryhmän luominen

Jos haluat luoda Julkaisuryhmä-ominaisuuden käyttöön sivustollasi Commerce-julkaisutyökaluissa, toimi seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Julkaisuryhmät**.
1. Valitse komentopalkin yläosassa **Uusi sivusto**.
1. Kirjoita **Luo julkaisuryhmä** -valintaikkunan **Julkaisuryhmän nimi** -kohtaan kuvaava nimi. Valitse sitten **OK**.

## <a name="set-the-publish-group-authoring-context"></a>Julkaisuryhmän sisällön luontikontekstin määrittäminen

Commercessa oletusarvoinen sisällönluontikonteksti on reaaliaikainen sivuston konteksti. Reaaliaikaisen sivuston luontikonteksti on oletusnäkymä, jossa voit tarkastella ja tehdä muutoksia suoraan verkkosivustoosi käyttämättä julkaisuryhmää. Se edustaa uusimpia suoria päivityksiä sivustosi julkaistuun versioon. Jos vasemmassa siirtymisruudussa olevassa **Julkaise ryhmät** -kohdan kontekstiohjausobjektissa näkyy **Live-sivusto**, työskentelet sivuston luontikontekstissa. **Reaaliaikainen sivusto** on kontekstiohjausobjektin oletusnimi. Muussa tapauksessa kontekstiohjausobjekti näyttää julkaisuryhmän nimen.

Jos haluat työskennellä julkaisuryhmässä, sinun on valittava sen sisällön julkaisukonteksti. Voit määrittää julkaisuryhmän kontekstin noudattamalla jotakin näistä vaiheista.

- Valitse vasemmasta siirtymisruudusta kontekstiohjausobjekti suoraan **Julkaisuryhmät**-kohdasta ja valitse sitten julkaisuryhmän nimi näkyviin tulevasta luettelosta. Kontekstiohjausobjekti on nimetty uudelleen ja näyttää julkaisuryhmän nimen.
- Valitse vasemmasta siirtymisruudusta **Julkaisuryhmät** ja valitse sitten **Julkaisuryhmät**-kohdassa julkaisuryhmän nimi. Kontekstiohjausobjekti on nimetty uudelleen ja näyttää julkaisuryhmän nimen.

Kun olet määrittänyt julkaisuryhmän sisällön luontikontekstin, työskentelet julkaisuryhmän kontekstissa, kun esikatselet ja muokkaat sivuston sisältöä.

Jos haluat palata oletusarvoiseen sivuston luontikontekstiin, valitse kontekstiohjausobjekti ja valitse sitten **Live-sivusto**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Sivujen tai muiden kohteiden lisääminen julkaisuryhmään

Kun olet valinnut julkaisuryhmän sisällönluontikontekstin ja vasemmanpuoleisen siirtymisruudun kontekstiohjausobjekti näyttää sen nimen, voit luoda sisältöä samalla tavalla kuin oletussivuston oletuskontekstissa. Voit myös lisätä aiemmin luotuja sivuja tai muita kohteita muista julkaisuryhmistä tai reaaliaikaisen sivuston kontekstista.

Voit kopioida aiemmin luodut sivut julkaisuryhmään seuraavasti.

1. Valitse kopioitavan sisällön luontikonteksti ja valitse sitten vasemmasta siirtymisruudusta **Sivut**.
1. Valitse julkaisuryhmään lisättävä sivu.
1. Valitse komentopalkissa **Kopioi julkaisuryhmään**.
1. Valitse **Valitse julkaisuryhmä** -valintaikkunassa julkaisuryhmä, johon haluat lisätä sivun, ja valitse sitten **OK**.

Samojen perusvaiheiden avulla voit luoda mukautettuja tuotesivuja, URL-osoitteita, malleja, asetteluja, fragmentteja ja mediakirjaston resursseja tai lisätä aiemmin luotuja kohteita julkaisuryhmään.

## <a name="validate-a-publish-group"></a>Julkaisuryhmän tarkistaminen

Jos haluat varmistaa, että kaikki julkaisuryhmän sisällön riippuvuudet täyttyvät ja että kaikki oikeellisuustarkistukset välitetään, voit suorittaa oikeellisuustarkistuksen ja tunnistaa ongelmat, jotka on ratkaistava ennen julkaisutoiminnon ajoitusta.

Voit vahvistaa julkaisuryhmän ennen sen ajoitusta tekemällä seuraavat toimet.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Julkaisuryhmät**.
1. Valitse verkossa tarkistettavat julkaisuryhmät.
1. Valitse komentopalkin yläosassa **Tarkista**.

Oikeellisuustarkistus suoritetaan kaikelle julkaisuryhmän sisällölle. Kaikki onnistuneet julkaisutoimet estävät ongelmat näkyvät ilmoitusruudussa, joka näkyy oikeassa yläkulmassa.

> [!NOTE]
> Oikeellisuustarkistus suoritetaan aina automaattisesti, kun julkaisuryhmä on ajoitettu. Komentopalkin **Vahvista** -painike on kuitenkin hyödyllinen, koska se auttaa tunnistamaan ongelmat, jotka on korjattava, ennen kuin yrität ajoittaa julkaisuryhmän julkaistavaksi.

## <a name="schedule-a-publish-group-to-go-live"></a>Julkaisuryhmän ajoittaminen Live-tilaan

Jos haluat ajoittaa julkaisuryhmän julkaistavaksi sivustollasi, toimi seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Julkaisuryhmät**.
1. Valitse **Julkaisuryhmät**-kohdassa ajastettava julkaisuryhmä.
1. Valitse komentopalkin yläosassa **Muokkaa aikataulua**. **Muokkaa aikataulua** -valintaikkuna tulee näkyviin.
1. Valitse päivämäärä ja kellonaika, jolloin julkaisuryhmä siirtyy Live-tilaan, ja valitse sitten **OK**.

Jos haluat poistaa julkaisuryhmän ajoituksen, noudata samoja vaiheita, mutta valitse **Muokkaa aikataulua** -valintaikkunasta **Peruuta julkaisuryhmä**.

> [!NOTE]
> Erittäin suurien julkaisuryhmien julkaisu voi kestää jopa minuutin tai kaksi, kun on niiden aikataulunmukainen aika. Huomaa, että julkaisutoiminto ei ole hetkellinen ja että pienemmät julkaisuryhmät julkaistaan nopeammin.

## <a name="publish-groups-faq"></a>Julkaisuryhmien usein kysytyt kysymykset

**Kuinka monta kohdetta julkaisuryhmässä voi olla?**

Tällä hetkellä voi olla enintään 2 000 kohdetta julkaisuryhmää kohti. Huomaa, että erittäin suurien julkaisuryhmien julkaisu voi kestää useita minuutteja, kun on niiden aikataulunmukainen aika.

**Ovatko julkaisuryhmät, kuten koodi"sivuliikkeet", ohjelmistokehityksen terminologiassa?**

Kyllä ja ei. Julkaisuryhmiä voidaan ajatella sivustosi haaraversioina. Näin ne toimivat kuin oksat. Yhdistämisen käsitettä ei kuitenkaan ole yksittäisten nimikkeiden tasolla. Viimeksi julkaistu kohde korvaa sen, mitä aiemmin oli olemassa, ja viimeisin julkaisutoiminto ohittaa aina aiemmat julkaisutoiminnot.

**Voinko ajoittaa kaksi julkaisuryhmää siirtymään Live-tilaan samaan aikaan?**

Nro Suorituskyky- ja ristiriitasyistä järjestelmä pakottaa sinut porrastamaan ajoitettuja julkaisuryhmiä vähintään viiden minuutin välein.

**Voinko ajoittaa monikanavaisia taustajärjestelmäkohteita, kuten alennuksia ja tuotepäivityksiä, käyttämällä julkaisuryhmiä?**

Tällä hetkellä julkaisuryhmät-ominaisuus tukee vain verkkosivuston sisältöä. Microsoft on kuitenkin tietoinen siitä, että integrointi taustajärjestelmämarkkinointiskenaarioihin voisi olla arvokasta monikanavaisen kampanjan lanseerauksessa ja automatisoinnissa.

## <a name="additional-resources"></a>Lisäresurssit

[Tapoja lisästä sisältöä](add-manage-content.md)

[Sivumallisanasto](page-elements-overview.md)

[Asiakirjan tilat ja elinkaari](document-states-overview.md)

[Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen](cross-channel-sharing.md)

[Moduulien käyttäminen](work-with-modules.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Sivuston selauksen mukauttaminen](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
