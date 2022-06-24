---
title: Varastotyön valvonta työmallien ja sijaintidirektiivien avulla
description: Tässä artikkelissa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ suoritetaan varastossa.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65675d8a99d023176e3e66e92cd3d634750bdb0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877418"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Varastotyön valvonta työmallien ja sijaintidirektiivien avulla

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ suoritetaan varastossa.

Ohjeet, jotka varastotyöntekijät saavat mobiililaitteessa, määräytyvät Dynamics 365 Supply Chain Managementissa määrittämiesi työmallien mukaisesti. Työmallit määrittävät, miten kunkin varastoprosessin työt suoritetaan. Linkittämällä sijaintidirektiivin työmalleihin, voit varmistaa, että työ tapahtuu tietyillä fyysisillä varastojen alueilla.

## <a name="work-templates"></a>Työmallit

**Työmallit**-sivun avulla voit määrittää työtoiminnot, jotka on suoritettava varastossa. Yleensä varastotyötoiminnot kostuvat toimintopareista: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sitten keräillyt varastotuotteet toiseen paikkaan. 

Työmallit koostuvat otsikosta ja siihen liittyvistä riveistä. Jokainen työmalli on tarkoitettu määrätylle *työtilaustyypille*. Monet työtilaustyypit on liitetty lähdeasiakirjoihin, kuten osto- tai myyntitilauksiin. Muut työtilaustyypit kuitenkin edustavat erillisiä varastoprosesseja kuten inventointia. *työpoolin tunnuksen* avulla voit järjestää työsi ryhmiin. 

Määritä työotsikon määrityksen asetuksilla, milloin uusi työkappale on luotava. Voit esimerkiksi määrittää keräilyrivien maksimimäärän ja odotetun keräilyajan maksimimäärän. Tämän jälkeen, jos myyntitilauksen keräilyprosessin työ ylittää jommankumman näistä arvoista, työ jaetaan kahdeksi työkappaleeksi.

Määritä **Työn otsikoiden katkaisut** -painikkeella, milloin järjestelmän on luotava uudet työotsikot. Kullekin _tilausnumerolle_ esimerkiksi luodaan työotsikko valitsemalla toimintoruudussa **Muokkaa kyselyä** ja lisäämällä sitten **Tilausnumero**-kenttä kyselyeditorin **Lajittelu**-välilehteen, **Lajittelu**-välilehteen lisätyt kentät ovat valittavissa *ryhmittelykenttinä*. Määritä ryhmittelykenttä valitsemalla toimintoruudussa **Työotsikon katkaisut** ja valitse sitten jokaiselle ryhmittelykenttänä käytettävälle kentälle valintaruutu **Ryhmittele tämän kentän mukaan** -sarakkeessa.

Työrivit ilmaisevat fyysisiä tehtäviä, jotka tarvitaan työn käsittelemiseen. Esimerkiksi lähtevässä varastoprosessissa saattaa olla yksi työrivi varastossa olevien nimikkeiden keräilyyn ja toinen rivi näiden nimikkeiden sijoittamiseen valmistelualueelle. Tämän jälkeen voi olla lisärivi nimikkeiden keräilyyn valmistelualueelta ja toinen rivi näiden nimikkeiden asettamiseen kuorma-autoon lastausprosessin osana. Voit määrittää *direktiivikoodin* työmallirivillä. Direktiivikoodi linkitetään sijaintidirektiiviin ja se auttaa siten varmistamaan, että varastotyö käsitellään varaston oikeassa sijainnissa.

Voit määrittää kyselyn ohjaamaan, milloin määrättyä työmallia käytetään. Voit esimerkiksi määrittää rajoituksen siten, että määrättyä mallia voidaan käyttää työhön vain määrätyssä varastossa. Vaihtoehtoisesti käytössä voi olla useita malleja, joita käytetään työn luomiseen lähtevän myyntitilauksen käsittelyyn riippuen myynnin alkuperästä. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien työmallien arviointijärjestyksen. Siksi, jos sinulla on erityinen kysely tietylle työmallille, anna sille alhainen järjestysnumero. Tämä kysely arvioidaan sitten ennen muita, yleisiä kyselyitä.

> [!NOTE]
> Voit estää järjestelmää korvaamasta automaattisesti työmallin *järjestysnumeroita* mallin poistamisen jälkeen ottamalla *Säilytä työmallin järjestysnumerot poistettaessa* -toiminto käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Voit lopettaa tai keskeyttää työprosessin työrivin **Pysäytä työ** -asetuksen avulla. Siinä tapauksessa työn suorittavaa työntekijää ei pyydetä suorittamaan seuraavaa työrivin vaihetta. Siirtyäkseen seuraavaan vaiheeseen, työntekijän on valittava työ uudelleen. Voit myös erotella tehtävät työkappaleen sisällä käyttämällä eri *työluokan tunnusta* työmallin riveillä.

## <a name="location-directives"></a>Sijaintidirektiivit

Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään ja minne kerätyt nimikkeet sijoitetaan. Sijaintidirektiivit koostuvat otsikosta ja siihen liittyvistä riveistä. Luot ne **Sijaintidirektiivi**-sivulla.

Otsikossa jokaisen direktiivin on oltava liitettynä *työtilaustyypille*. Se määrittää varastotapahtuman tyypin, johon direktiiviä tullaan käyttämään, kuten myyntitilaukset, täydennys, tai raaka-aineiden keräily. *työtyyppi* määrittää, käytetäänkö sijaintidirektiiviä keräily- tai poispanotyöhön, tai johonkin muuhun varastoprosessiin kuten laskentaan tai varaston tilan muutoksiin. Sinun on myös määritettävä *toimipaikka* ja *varasto*. Otsikossa määrittämääsi *direktiivikoodia* voidaan käyttää linkittämään sijaintidirektiivin yhteen tai useampaan työmalliin. 

Mitä tulee työmalleihin, voit määrittää kyselyn tunnistamaan, milloin määrättyä sijaintimallia käytetään. Voit esimerkiksi määrittää, että silloin, kun sähköinen kaupankäynti on myyntitilauksen alkuperä, varasto on keräiltävä määrätyltä varaston alueelta. Järjestelmä käyttää **järjestysnumero**-kenttää määrittämään käytettävissä olevien sijaintidirektiivien arviointijärjestyksen.

Sijaintidirektiivin rivit asettavat lisärajoituksia sijainnin löytämissääntöjen käytölle. Voit määritellä vähimmäis- ja enimmäismäärät, joihin direktiiviä tulisi soveltaa ja voit määrittää, että direktiivi koskee määrättyä varastoyksikköä. Esimerkiksi jos mittayksikkö on kuormalava, kuormalavojen nimikkeet voidaan asettaa tiettyyn paikkaan. Voit myös määrittää, voidaanko määrä jakaa eri sijainteihin. Samoin kuin sijaintidirektiivin otsikolla, kullakin sijaintidirektiivin rivillä on järjestysnumero, joka määrittää näiden rivien arviointijärjestyksen.

Sijaintidirektiiveillä on yksi yksityiskohtien taso lisää: *sijaintidirektiivin toiminnot*. Voit määrittää useita sijaintidirektiivin toimintoja kullekin riville. Jälleen kerran järjestysnumeroa käytetään määrittämään järjestys, jossa arvioidaan toimia. Tällä tasolla voit määrittää kyselyn määrittääksesi, miten löydetään paras sijainti varastossa. Voit myös käyttää esimääritettyjä **Strategia**-asetuksia parhaan sijainnin löytämiseen.

Lisä tietoja sijaintidirektiivien luomisesta ja konfiguroinnista on kohdassa [Sijaintidirektiivin luominen](create-location-directive.md).

### <a name="how-location-directives-work"></a>Sijaintidirektiivien käyttäminen

Sijaintidirektiivit määrittävät, *missä* nimikkeet kerätään ja *mihin* ne asetetaan. Järjestelmä arvioi sijaintidirektiiviä kunkin työrivin perusteella ja valitsee sitten sijainnin työrivin tietojen perusteella. Järjestelmä etsii kaikki tiettyä työriviä vastaavat sijaintidirektiivit. (Ne ovat esimerkiksi oikealle varastolle ja vastaavat kyselyä.) Se arvioi sitten järjestyksessä löydetyt direktiivit.

> [!NOTE]
> Keräily- ja asetussijainnit valitaan valmiiksi joissakin erityistapauksissa. Esimerkiksi _oston rekisteröinnin_ aikana ensimmäinen keräily on aina sijainnista, jossa rekisteröinti tehdään. Toinen esimerkki on *varastosiirto mallin perusteella*, jossa varastotyöntekijä valitsee keräilysijainnin ja vain asetussijainnit etsitään sijaintidirektiiveillä.

## <a name="additional-resources"></a>Lisäresurssit

- Video: [Perusteellinen varastonhallinnan määrityksen tarkastelu](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Ohjeartikkeli: [Sijaintidirektiivien käsitteleminen](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]