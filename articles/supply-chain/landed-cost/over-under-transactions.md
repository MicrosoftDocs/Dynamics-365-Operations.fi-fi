---
title: Ylitys-/alitustapahtumat
description: Tässä ohjeaiheessa on tietoja, jotka auttavat ylitys-/alitustapahtumien käytäntöjen tietojen määrittämisessä, jotta järjestelmä voi määrittää, miten tuotteiden yli- ja alikäsittelyä hallitaan vastaanoton hetkellä.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ef9575d2b6dbb5c12912624544cb4a3508601237e6f49150d13b31786bb76877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777932"
---
# <a name="overunder-transactions"></a>Ylitys-/alitustapahtumat

[!include [banner](../../includes/banner.md)]

Kun matkan tilaukset on käsitelty, järjestelmä odottaa lopullisessa kohdevarastossa käytettäväksi vastaanotetun nimikemäärän vastaavan määrää, joka on määritetty matkaan liittyvillä ostotilausriveillä. Koska ostotilausrivien tarkkaa määrää ei kuitenkaan aina vastaanoteta varastoon, **Aiheutunut kustannus** -moduuli määrittää sääntöjoukon, jota käytetään liiallisen tai liian vähäisen tuotemäärän vastaanoton käsittelyyn. Nämä säännöt ovat erityisen tärkeitä, koska alkuperäinen ostotilaus on laskutettu eikä sitä enää voi muuttaa. Kun ylitys-/alitustapahtumien käytäntöjen tiedot määritetään, järjestelmä voi määrittää, miten tuotteiden yli- ja alikäsittelyä hallitaan vastaanoton hetkellä. Voit hallita liiallista tai liian vähäistä varastoa myös käyttämällä **Ylitys-/alitustapahtumat**-sivua.

## <a name="overunder-tolerances"></a>Ylitys- ja alitustoleranssit

Määrität ylitoimituksen ja alitoimituksen toleranssit määrittääksesi ne liialliset ja liian vähäiset määrät tai tilavuudet, jotka voidaan matkan osalta käsitellä aiheuttamatta virhettä. Jos matkarivin vastaanotto ei ole näiden toleranssien puitteissa, sitä on muutettava ja se on ratkaistava, ennen kuin matkarivi voidaan sulkea lisäkäsittelyä varten.

Voit määrittää toleranssit valitsemalla **Aiheutunut kustannus \> Yli-/alitoimituksen määritys \> Ylitys/alitustoleranssit**. Siellä voit tarkastella, muokata, lisätä ja poistaa toleranssitietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Tilikoodi | <p>Määritä ne toimittajat, joihin toleranssi pätee, valitsemalla jokin seuraavista arvoista:</p><ul><li>**Taulukko** – Ylitys-/alitustoleranssi pätee vain riville valittuun toimittajaan.</li><li>**Ryhmä** – Ylitys-/alitustoleranssi pätee kaikkiin riville valitun toimittajien toleranssiryhmän toimittajiin.</li><li>**Kaikki** – Ylitys-/alitustoleranssi pätee kaikkiin toimittajiin.</li></ul> |
| Tilisuhde | Valitse toimittaja tai toimittajaryhmä, johon ylitys-/alitustoleranssi pätee, sen arvon perusteella, joka on valittu **Asiakkuuskoodi**-kentässä. |
| Nimikekoodi | <p>Määritä ne nimikkeet, joihin toleranssi pätee, valitsemalla jokin seuraavista arvoista:</p><ul><li>**Taulukko** – Ylitys-/alitustoleranssi pätee vain riville valittuun nimikkeeseen.</li><li>**Ryhmä** – Ylitys-/alitustoleranssi pätee kaikkiin riville valitun nimikkeiden toleranssiryhmän nimikkeisiin.</li><li>**Kaikki** – Ylitys-/alitustoleranssi pätee kaikkiin nimikkeisiin.</li></ul> |
| Nimikkeen suhde | Valitse nimike tai nimikeryhmä, johon ylitys-/alitustoleranssi pätee, sen arvon perusteella, joka on valittu **Nimikekoodi**-kentässä. |
| Summan toleranssi | Määritä määrätoleranssi, jota sovelletaan koko ostotilaukseen. |
| Prosenttiarvotoleranssi | Määritä prosentuaalinen toleranssi, jota sovelletaan yksittäiseen ostotilausriviin. |

## <a name="overunder-reasons"></a>Ylityksen/alituksen syyt

Kun vastaanotettuun matkariviin liittyy liian suuri tai liian pieni määrä, liian suuren tai liian pienen määrän syy voi olla tarpeen määrittää. Tällöin voit valita vastaanottoriviltä yli- tai alitoimituksen syyn, kun tuotteet on vastaanotettu.

Voit määrittää yli- ja alitoimitusten syyt valitsemalla **Aiheutunut kustannus \>Ylityksen/alituksen määritys \> Ylityksen/alituksen syyt**. Siellä voit tarkastella, muokata ja poistaa käytettävissä olevia yli- ja alitoimituksen syitä. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin syyn osalta.

| Kenttä | kuvaus |
|---|---|
| Ylityksen/alituksen syy | Syötä yksilöllinen nimi liian suuren tai liian pienen vastaanottotapahtuman syylle. |
| kuvaus | Syötä ylityksen/alituksen syylle kuvaus. |
| Siirto | Valitse ylityksen/alituksen syyhyn liittyvä siirron kirjauskansio. Tämä kenttä sisältää luettelon kaikista käytettävissä olevista kirjauskansiosta, joihin *Siirto*-tyyppinen kirjauskansio on yhdistetty **Varaston kirjauskansioiden nimet** -sivulla (**Varastonhallinnan määritys \> Kirjauskansioiden nimet \> Varasto**). |

## <a name="item-overunder-tolerance-groups"></a>Nimikkeen ylitys- ja alitustoleranssiryhmät

Nimikkeet, joilla on samat toleranssit, voidaan ryhmitellä yhteen. Näin voit määrittää ryhmän kaikkien nimikkeiden ylitys-/alitustoleranssin samanaikaisesti.

Voit määrittää nimikkeiden ylitys-/alitustoleranssiryhmiä valitsemalla **Aiheutunut kustannus \>Ylityksen/alituksen määritys \> Nimikkeen ylitys-/alitustoleranssiryhmät**. Siellä voit tarkastella, muokata, lisätä ja poistaa ylitys-/alitustoleranssiryhmien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Ylitys- ja alitustoleranssiryhmä | Syötä ryhmälle yksilöllinen nimi. Valitse nimi, joka kuvaa toleranssia, kuten *1% Var*. |
| kuvaus | Anna ryhmän kuvaus. |

## <a name="vendor-overunder-tolerance-groups"></a>Toimittajan ylitys- ja alitustoleranssiryhmät

Voit ryhmitellä yhteen toimittajia, jotka toimittavat säännöllisesti liikaa tai liian vähän. Tämän jälkeen voit määrittää ryhmän ylitys-/alitustoleranssin.

Voit määrittää toimittajien ylitys-/alitustoleranssiryhmiä valitsemalla **Aiheutunut kustannus \>Ylityksen/alituksen määritys \> Toimittajien ylitys-/alitustoleranssiryhmät**. Siellä voit tarkastella, muokata, lisätä ja poistaa ylitys-/alitustoleranssiryhmien tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Ylitys-/alitusryhmät | Syötä ryhmälle yksilöllinen nimi. Valitse nimi, joka kuvaa ryhmään kuuluvia toimittajia. |
| kuvaus | Anna ryhmän kuvaus. |

## <a name="view-and-process-overunder-transactions"></a>Ylitys-/alitustapahtumien tarkastelu ja käsittely

Ylitys-/alitustapahtumia luodaan, kun poispantujen tuotteiden määrä ei vastaa alustettua määrää. Saapumisten kirjauskansion määrää pitäisi päivittää ainoataan poispannulla määrällä.

Kun matkarivien vastaanottoa käsitellään, toimittajille voidaan määrittää ylitys-/alitustoleransseja. Tämän jälkeen nimikkeet tarkistetaan ja vahvistetaan. Toleranssi voidaan määrittää prosenttiosuutena, paikallisena summana tai molempina.

Jos vastaanotettu nimike on toleranssin sisällä, järjestelmä luo siirtokirjauskansion. Tämä kirjauskansio voidaan määrittää matkan parametrisivulla. Lisäksi luodaan ylitys-/alitustapahtuma. Otetaan esimerkiksi 100 euron tilausarvo, jota vastaava vastaanoton arvo on 99 euroa ja täyttää toleranssisäännöt. Tällöin luodaan negatiivinen siirtokirjauskansio liian vähäiselle vastaanotetulle määrälle.

Jos vastaanotettu nimike ei ole toleranssin puitteissa, järjestelmä luo määräeroavaisuudelle ylitys-/alitustapahtuman.

Voit tarkastella ja käsitellä ylitys-/alitustapahtumia valitsemalla **Aiheutunut kustannus \> Kyselyt \> Ylitys-/alitustapahtumat**. Siellä ylitys-/alitustapahtuma liitetään kaikkiin niihin matkan nimikkeisiin, joita on vastaanotettu liikaa tai liian vähän. On suositeltavaa käyttää **Ylitys-/alitustapahtumat**-sivua kaikkien matkoihin liittyvien ylitys-/alitustapahtumien ratkaisemiseen. On myös suositeltavaa, että siirto- tai laskentakirjauskansioita **ei** käytetä liian vähäisten varastotoimitusten manuaaliseen ratkaisemiseen. Sen sijaan kannattaa käyttää **Ylitys-/alitustapahtumat**-sivua liian vähäisten varastotoimitusten määrien hallintaan.

### <a name="upper-overview-tab"></a>Ylempi yleiskatsausvälilehti

Voit tarkastella ylitys-/alitustapahtumia valitsemalla **Ylitys-/alitustapahtumat**-sivun yläosan **Yleiskatsaus**-välilehden. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä ruudukossa.

| Kenttä | kuvaus |
|---|---|
| Ylitys-/alitustapahtuman numero | Ylitys-/alitustapahtumatietueen yksilöllinen nimi, joka on luotu automaattisesti saapumisten kirjauskansion käsittelemisen yhteydessä. |
| Matka | Matka, johon ostorivi oli liitettynä. |
| Lähetyskontti | Kuljetuskontti, johon ostorivi oli liitettynä. |
| Saapumisen kirjauskansio | Saapumisten kirjauskansio, jonka perusteella ylitys-/alitusrivi on luotu. |
| Viite | Viittaus joko ylitys-/alitustapahtuman ostotilaukseen tai siirtotilaukseen. |
| Numero | Ostotilaus, johon ylitys-/alitustapahtumassa viitataan. |
| Toimittajanro | Toimittaja, johon ylitys tai alitus liittyy. |
| Matkalla olevien tavaroiden numero | Kuljetettavan tuotteen numero, jos sellainen on. |
| Nimiketunnus | Nimikenumero, johon ylitys tai alitus liittyy. |
| Alkuperäinen määrä | Lähetykseen liitetyn ostotilausrivin alkuperäinen määrä. |
| Vastaanotettu määrä | Määrä, joka todella vastaanotettiin. |
| Ero | Odotetun saapumisten kirjauskansion määrän ja saapumisten kirjauskansioon kirjatun määrän välinen ero. Negatiivinen arvo tarkoittaa tuotteiden ylitoimitusta. |
| Jäljelle jäävä määrä | Määrä, joka jää saapumisten kirjauskansion riville. |
| Yli-/alitoimitus | Arvo, joka ilmaisee, onko vastaanotettu määrä ylitys vai alitus. |
| Tila | Ylitys-/alitustapahtuman tila. Riippuen **[Aiheutuneen kustannuksen parametrit](landed-cost-parameters.md)** -sivun asetuksista ylitoimitus voi johtaa automaattisesti siirtokirjauskansion luomiseen ylitoimitetulle määrälle ja sen kirjauskansioon kirjaamiseen. Tällöin ylitys-/alitustapahtuman tilana on *Valmis*. Jos tuotteiden alitoimitusvarastosta siirtäminen edellyttää toimenpiteitä, tietueen tilana on *Käynnissä*. |
| Ylityksen/alituksen syy | Syy, joka on määritetty ylitys-/alitustapahtumalle. |
| Muut varastodimensiot | Voit näyttää ruudukossa sarakkeita lisädimensioille tarpeen mukaan. Näitä dimensioita ovat esimerkiksi eränumero, varastotila ja varasto. Valitse toimintoruudussa **Varasto \> Näytä dimensiot** ja avaa valintaikkuna, jossa voit valita sisällytettävät dimensiot. |

### <a name="upper-general-tab"></a>Ylempi Yleistä-välilehti

Voit tarkastella lisätietoja rivistä, joka kulloinkin on valittuna ylemmässä **Yleiskatsaus**-välilehdessä, valitsemalla **Yleistä**-välilehden **Ylitys-/alitustapahtumat**-sivun yläosasta. Tämän välilehden tiedot sisältävät kaikkien käytettävissä olevien dimensioiden arvot. Nämä tiedot noudetaan alkuperäisestä ostotilauksesta.

### <a name="lower-overview-tab"></a>Alempi yleiskatsausvälilehti

Voit sen rivin asiakirjatyypin, joka kulloinkin on valittuna ylemmässä **Yleiskatsaus**-välilehdessä, valitsemalla **Yleiskatsaus**-välilehden **Ylitys-/alitustapahtumat**-sivun alaosasta. Seuraavassa taulukossa näkyvät valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Uusi asiakirjatyyppi | Tämän kentän arvona on joko *Siirtokirjauskansio* tai *Ostotilaus* sen toiminnon mukaan, joka näytettään valitulla ylitys-/alitustapahtuman rivillä. |
| Numero | Viittaus ja linkki joko valitun ylitys-/alitustapahtuman riviin liittyvään ostotilaukseen tai siirtokirjauskansioon. |
| Ylityksen/alituksen syy | Syy, joka on määritetty valitulle ylitys-/alitustapahtumariville. |
| Määrä | Määrä, jonka olet valinnut joko valitun ylitys-/alitustapahtuman riviin liittyvälle ostotilaukselle tai siirtokirjauskansiolle. |

### <a name="lower-general-tab"></a>Alempi Yleistä-välilehti

Voit tarkastella ylitys-/alitustapahtuman numeroa, erätunnusta ja dimensionumeroa, jotka liittyvät valittuun ylitys-/alitustapahtumariviin, valitsemalla **Yleistä**-välilehden **Ylitys-/alitustapahtumat**-sivun alaosassa. 

### <a name="process-overunder-transactions"></a>Ylitys-/alitustapahtumien käsittely

**Ylitys-/alitustapahtumat**-sivun toimintoruutu sisältää seuraavat komennot sivulla valittujen tapahtumien käsittelemistä varten. Näiden komentojen avulla voit valita, miten kukin tapahtuma käsitellään.

- **Luo \> Siirto** – Luo ja kirjaa siirtokirjauskansio valitulle tapahtumalle. Alitustapahtumien osalta luodaan ja kirjataan automaattisesti siirtokirjauskansio erotukselle odotetun ja todellisen vastaanotetun määrän välillä. Valitse tämä komento ylitystapahtumille, jos haluat, että toimittaja saa kustannuseron tiedoksi.
- **Luo \> Ostotilaus** – Luo ostotilaus erotukselle valitun tapahtuman erotukselle odotetun ja todellisen vastaanotetun määrän välillä. Valitse tämä komento ylitystapahtumille, jos haluat, että organisaatiosi saa kustannuseron tiedoksi.
- **Luo \> Siirto kohteeseen** – Tätä komentoa voi käyttää vain siirtotilauksiin. Valitse tämä vaihtoehto, jos haluat siirtää liiallisen tai liian vähäisen määrän kohdevarastoon.
- **Luo \> Siirto lähtöpaikkaan** – Tätä komentoa voi käyttää vain siirtotilauksiin. Valitse tämä vaihtoehto, jos haluat siirtää liiallisen tai liian vähäisen määrän lähtövarastoon.
