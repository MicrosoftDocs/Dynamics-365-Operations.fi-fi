---
title: Inventory Visibilityn varaukset
description: Tässä artikkelissa käsitellään varausominaisuuden määrittämistä luomaan varauksia, käyttämään varauksia ja/tai poistamaan määritettyjen varastomäärien varauksia varaston näkyvyyssovelluksella.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762719"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibilityn varaukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan alustavien varausten normaalista käyttötapauksesta ja alustavien varausten määrittämisestä Inventory Visibility -sovelluksessa. Artikkelissa on tietoja alustavien varausten luomisesta, niiden vastakirjauksesta fyysiseen kulutukseen sekä tiettyjen varastomäärien muokkaamisesta ja varauksen poistosta.

## <a name="sample-use-case-for-soft-reservation"></a>Alustavan varauksen esimerkkikäyttötapaus

Alustavien varausten avulla organisaatiot voivat saada käytettävissä olevalle varastolle yhden tietolähteen erityisesti tilausten täyttämisprosessin ajaksi. Nämä toiminnot ovat hyödyllisiä organisaatioille seuraavien olosuhteiden vallitessa:

- Organisaatiolla on vähintään kaksi eri järjestelmää, jotka vastaanottavat suoraan ulkoisia tilauksia.
- Organisaatio on erittäin tarkka ja haluaa estää tuotevaraston päällekkäiset varaukset. Näin voi tapahtua, jos useat järjestelmät voivat varata varaston viimeisen kappaleen. Tämä tilanne voidaan estää, jos kaikki tilausjärjestelmät voivat tehdä välittömän alustavan varauksen ohjelmointirajapintakutsuja Inventory Visibility -sovellukseen. Tämä tarjoaa yhden tietolähteen varaston näkyvyyteen.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Inventory Visibilityn alustavat varaukset" width="720" />](media/inventory-visibility-soft-reservation.png)

Edellisessä kuvassa näytetään, miten alustava varaus toimii. Siinä näkyvät seuraavat toiminnot korostettuina:

- Alkuperäinen varastotaso synkronoidaan Inventory Visibility -sovellukseen Microsoft Dynamics 365 Supply Chain Managementista.
- Alustavat varaukset kirjataan kustakin tilauskanavasta tai -järjestelmästä Inventory Visibility -sovellukseen. Inventory Visibility tarkistaa varaston saatavuuden ja yrittää tehdä alustavan varauksen. Jos alustava varaus onnistuu, Inventory Visibility lisää alustavan varauksen määrän, vähentää sen varattavissa olevasta määrästä ja vastaa alustavan varauksen tunnuksella.
- Tällöin fyysisen varaston määrä pysyy samana.
- Voit tämän jälkeen synkronoida yhden tai koostetun alustavasti varatun tilauksen (tilausrivit) Supply Chain Managementiin ja tehdä kiinteitä varauksia sekä vapauttaa ne varastoon tai päivittää lopullisen varaston määrän.
- Voit määrittää järjestelmän [vastakirjaamaan alustavat varaukset](#offset-scm), kun fyysinen varasto päivitetään Supply Chain Managementiin.

Alustavat varaukset yleensä luodaan, niitä käytetään ja ne peruutetaan käyttämällä ohjelmointirajapintakutsuja Inventory Visibility -palveluun.

> [!NOTE]
> Supply Chain Management (ja muut kolmannen osapuolen järjestelmät) voidaan lisäksi määrittää tekemään vastakirjaus varatulle määrälle Inventory Visibility -sovelluksen avulla. Vastakirjausmäärä poistetaan varaustietueista varaston näkyvyyssovelluksessa.
>
> Oletusarvoisesti vastakirjaustoiminto otetaan automaattisesti käyttöön, kun alustavan varauksen ominaisuus otetaan käyttöön.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Varausominaisuuden käyttöönotto ja määritys

Varausominaisuus otetaan käyttöön seuraavasti:

1. Kirjaudu Power Appsiin ja avaa **Inventory Visibility**.
1. Avaa **Määritykset**-sivu.
1. Ota *OnHandReservation*-ominaisuus käyttöön **Ominaisuuksien hallinta** -välilehdessä.
1. Kirjaudu sisään Supply Chain Management -ympäristöön.
1. Siirry **[Ominaisuuksienhallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**-työtilaan ja ota *Varaston näkyvyyden integrointi varauksen vastakirjaukseen* -ominaisuus käyttöön (vaatii version 10.0.22 tai sitä uudemman).
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integrointiparametrit**, avaa **Varauksen vastakirjaus**-välilehti ja määritä seuraavat asetukset:

    - **Ota varauksen vastakirjaus käyttöön** – Voit ottaa tämän toiminnon käyttöön asettamalla arvoksi *Kyllä*.
    - **Varauksen vastakirjauksen määre** – Valitse varaston tapahtuman tila, joka vastakirjaa Inventory Visibilityssa tehdyt varaukset. Tämä asetus määrittää tilauksen käsittelytilan, joka käynnistää vastakirjaukset. Vaihetta seurataan tilauksen varastotapahtuman tilan perusteella. Valitse jokin seuraavista:

        - *Tilauksessa* – Tilaukset, joiden tila on *Tilauksessa*, lähettävät vastakirjauspyynnön niiden luonnin yhteydessä. Vastakirjauksen määrä on luodun tilauksen (rivin) määrä.
        - *Varaus* – Tilaukset, joiden tila on *Varaus*, lähettävät vastakirjauspyynnön, kun ne varataan tilauksella tai fyysisesti. Kun *Varaus*-tilassa, tilaus lähettää vastakirjauspyynnön mille tahansa uudelle varaston tilalle, joka lähinnä varattua ja kerättyä (esimerkiksi kerätty, pakkausluettelo kirjattu tai laskutettu). Tämä toiminta tapahtuu, vaikka varaus ohitettaisiin Supply Chain Managementissa ja jatkettaisiin toisen varaston tilan parissa (esimerkiksi jos vapautus varastoon ohitetaan ja siirrytään keräykseen ja pakkaukseen). Pyyntö käynnistetään vain kerran. Jos se on käynnistetty keräilyn yhteydessä, se ei monista vastakirjausta pakkausluettelon kirjauksen yhteydessä. Vastakirjauksen määrä on sama kuin varastotapahtuman tilan määrä, kun vastakirjaus on käynnistetty (toisin sanoen *Tilaukseen varattu*/*Fyysinen varattu* tai myöhempi tila vastaavalla tilausrivillä).

1. Kirjaudu takaisin Inventory Visibility -sovellukseen. Siirry **Määritys**-sivulle ja tarkista **Alustava varaus** -välilehdessä alustavan varauksen oletushierarkia. Lisää hierarkiaan uusia dimensioita tarpeen mukaan.
1. Tarkastele oletusasetuksia **Määritä alustavan varauksen yhdistämismääritys** -osassa. Oletusarvoisesti alustavasti varatut varastomäärät tulee tallentaa tietolähteen `iv` kohteen `softreservephysical` fyysisenä mittana. Laskettu *Varattavissa*-mitta on yhdistetty mittaan `availabletoreserve`. Jos haluat päivittää lasketun `availabletoreserve` mitan, siirry **Määritys**-sivulle ja laajenna **Laskettu mitta** -välilehdessä laskettu mitta ja muokkaa sitä.

Lisätietoja: [Varaston näkyvyyden määritys](inventory-visibility-configuration.md).

> [!NOTE]
> Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavalla kuin indeksihierarkia varastosaldoa koskevissa kyselyissä, mutta sitä käytetään itsenäisesti siten, että käyttäjät voivat määrittää dimension tiedot ja tehdä aiempaa tarkempia varauksia.
>
> Alustavan varauksen historian pitäisi sisältää tunnukset `SiteId` ja `LocationId` komponentteina, koska ne muodostavat Inventory Visibilityn osionmäärityksen.

Lisätietoja varausten määrittämisestä: [Varausten määritys](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Varausominaisuuden käyttäminen varaston näkyvyyssovelluksessa

Kun varauksen ohjelmointirajapintaa kutsutaan, järjestelmää merkitsee tiettyjen tavaroiden ja määrien varauksen.

Tässä on esimerkkiskenaario ja ohjelmointirajapintakyselyn esimerkkitekstiosa. Yritys Contoso myy sähköisen kaupankäynnin sivustossa tuotetta D0002. Asiakas voi tehdä myyntitilauksen pienestä punaisesta kaapista sivustossa. Contoso päättää täyttää tämän tilauksen käyttämällä seuraavia dimensioita:

- Organisaation tunnus = usmf
- Sivusto = 1
- Varasto = 11
- Tuote = D0002
- Väri = punainen
- Koko = pieni

Contoso on jo määrittänyt ohjelmointirajapintayhteyden Inventory Visibility -sovellukseen omasta sähköisen kaupankäynnin järjestelmästään. Kun tilaus vastaanotetaan, järjestelmä käynnistää välittömästi ohjelmointirajapintakutsun ja tekee alustavan varauksen kaapista Inventory Visibilityssa.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Luo alustavat varaukset käyttämällä varauksen ohjelmointirajapintaa

Varauksia tehdään varaston näkyvyyspalvelussa lähettämällä POST-pyyntö palvelun URL-osoitteeseen, joka voi olla esimerkiksi `/api/environment/{environmentId}/onhand/reserve`.

Varauspyynnön tekstiosan on sisällettävä organisaation tunnus, tuotetunnus, varatut määrät ja dimensiot:

Kun kutsut varausten ohjelmointirajapintaa, voit ohjata varausten vahvistamista määrittämällä `ifCheckAvailForReserv`-totuusarvoparametrin pyynnön tekstiosassa. `True`-arvo tarkoittaa, että vahvistus vaaditaan, ja `False`-arvo, että vahvistusta ei vaadita. Oletusarvona on `True`.

Jos haluat perua varauksen tai poistaa tiettyjen varastomäärien varauksen, määritä määräsi negatiivinen arvo ja ohita vahvistus määrittämällä `ifCheckAvailForReserv`-parametrin arvoksi `False`.

Tässä on esimerkki pyynnön tekstiosasta, joka viittaa edellisen kontekstin myyntitilaukseen.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Onnistunut alustavan varauksen pyyntö palauttaa *alustavan varauksen tunnuksen* jokaiselle varaustietueelle. Alustavan varauksen tunnus ei ole yksittäisen alustavan varauksen tietueen yksilöllinen tunniste, vaan alustavan varauksen pyyntöön liittyvien tuotetunnuksen ja dimension arvojen yhdistelmä. Voit tallentaa alustavan varauksen tunnuksen tilausriville, kun synkronoit onnistuneesti varatut tilaukset Supply Chain Managementiin tai toiseen ERP-järjestelmään vastakirjausta varten.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Vastakirjauksen alustavat varaukset Supply Chain Managementissa

Voit vastakirjata alustavan varauksen määrän sen jälkeen, kun tilauksen määrä on fyysisesti vähennetty Supply Chain Managementissa tai toisessa ERP-järjestelmässä. Inventory Visibility tarjoaa valmiin alustavan varauksen vastakirjauksen integroinnin Supply Chain Managementin kanssa.

Vastakirjaa alustava varaus alla olevien ohjeiden avulla.

1. Kirjaudu Supply Chain Managementiin.
1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Luo ulkoinen myyntitilaus uudelleen ja lisää myyntirivi, joka käyttää täsmälleen samoja tuotetunnuksen, organisaation, toimipaikan, varaston ja dimensioiden arvoja.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä juuri syötetty myyntirivi ja valitse sitten työkalurivillä **Varasto \> Varauksen tunnus**.
1. Noudata seuraavia ohjeita:

    - Kopioi alustavan varauksen tunnus alustavan varauksen pyynnön vastauksesta ja liitä se **Varauksen tunnus** -kenttään.
    - Jätä **Varauksen tunnus** -kenttä tyhjäksi, mutta valitse **Varastopalvelun automaattinen vastakirjaus** -valintaruutu. Järjestelmä määrittää automaattisesti, mitä tuotteita tai tuotedimensioita vastakirjataan niiden nimiketunnuksen ja dimension arvojen perusteella, jotka on syötetty valitulle riville.

1. Valitse **OK**.
1. Saman myyntirivin ollessa valittuna voit varata fyysisesti tilatun määrän valitsemalla **Varasto \> Varaus** **Myyntitilausrivit** -pikavälilehden työkalurivillä.
1. Jos olet aiemmin määrittänyt **Varauksen vastakirjauksen määre** -kentän arvoksi *Varattu*, vastakirjaus käynnistetään, kun tilausrivin tila on *Varaa fyysinen* tai *Varaa tilatut*. Erätyö suoritetaan kerran minuutissa vastakirjauksen pyyntöjen synkronoimiseksi Supply Chain Managementista Inventory Visibilityyn.

> [!NOTE]
> Jos tapahtuman tilat sisältävät määritetyn varauksen vastakirjauksen määreen, tapahtuman päivitys luo vastakirjauksen vastaavalle varaustietueelle, kun kaikki seuraavat ehdot täyttyvät:
>
> - Varastotapahtuman varaustunnus vastaa Inventory Visibilityssa olevaa varaustietueen varaustunnusta.
> - Varastotapahtuman dimensiot vastaavat Inventory Visibilityssa olevia varaustietueen dimensioita.
> - Varastotapahtuman tilan muutokset käynnistävät varausten vastakirjauksen, kun varastotapahtuman tila ilmaisee, että tilausprosessi on valmistunut tai se on ohitettu.

Vastakirjausmäärät seuraavat varastomääriä, jotka määritetään asiaankuuluvissa varastotapahtumissa. Vastakirjaus tehdään vain, jos varattu määrä jää Inventory Visibilityyn.

### <a name="cancel-or-revert-a-soft-reservation"></a>Alustavan varauksen peruuttaminen tai palauttaminen

Jos alkuperäinen tilausrivi peruutetaan tai poistetaan ja vastaava alustava varaus on palautettava, kirjaa negatiivinen määrä, jolla on täsmälleen samat tiedot ohjelmointirajapintakyselyn tekstiosassa.
