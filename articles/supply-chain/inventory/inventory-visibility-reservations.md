---
title: Varaston näkyvyyden varaukset
description: Tässä aiheessa käsitellään varausominaisuuden määrittämistä luomaan varauksia, käyttämään varauksia ja/tai poistamaan määritettyjen varastomäärien varauksia varaston näkyvyyssovelluksella.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5e6752539a6381e1f7271883102391374e04f3aa
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061701"
---
# <a name="inventory-visibility-reservations"></a>Varaston näkyvyyden varaukset

[!include [banner](../includes/banner.md)]


Tässä aiheessa käsitellään varausominaisuuden määrittämistä luomaan varauksia, käyttämään varauksia ja/tai poistamaan määritettyjen varastomäärien varauksia varaston näkyvyyssovelluksella.

Varauksilla merkitään varastomäärä, joka käytetään myöhemmin. Varausta luotaessa järjestelmä estää muita tilauksia varaamasta tai käyttämästä varattuja tavaroita siihen saakka, että varaus joko käytetään tai varaus poistetaan. Varaukset luodaan, niitä käytetään ja ne peruutetaan käyttämällä ohjelmointirajapintakutsuja varaston näkyvyyspalveluun.

Microsoft Dynamics 365 Supply Chain Management (ja muut kolmannen osapuolen järjestelmät) voidaan lisäksi määrittää tekemään vastakirjaus varatulle määrälle varaston näkyvyyssovelluksen avulla. Vastakirjausmäärä poistetaan varaustietueista varaston näkyvyyssovelluksessa.

Kun varaustoiminto otetaan käyttöön, Supply Chain Management on automaattisesti valmis tekemään vastakirjaus varauksille, jotka tehdä varaston näkyvyyssovelluksella.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Varausominaisuuden käyttöönotto ja määritys

Varausominaisuus otetaan käyttöön seuraavasti:

1. Kirjaudu Power Appsiin ja avaa **Varaston näkyvyys**.
1. Avaa **Määritykset**-sivu.
1. Ota *OnHandReservation*-ominaisuus käyttöön **Ominaisuuksien hallinta** -välilehdessä.
1. Kirjaudu Supply Chain Managementiin.
1. Siirry **[Ominaisuuksienhallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**-työtilaan ja ota *Varaston näkyvyyden integrointi varauksen vastakirjaukseen* -ominaisuus käyttöön (vaatii version 10.0.22 tai sitä uudemman).
1. Siirry kohtaan **Varastonhallinta \> Määritys \> Varaston näkyvyyden integrointiparametrit**, avaa **Varauksen vastakirjaus**-välilehti ja määritä seuraavat asetukset:
    - **Ota varauksen vastakirjaus käyttöön** – Voit ottaa tämän toiminnon käyttöön asettamalla arvoksi *Kyllä*.
    - **Varauksen vastakirjauksen muuttuja** – Valitse varaston tapahtumatila, joka vastakirjaa varaston näkyvyydessä tehdyt varaukset. Tämä asetus määrittää tilauksen käsittelytilan, joka käynnistää vastakirjaukset. Vaihetta seurataan tilauksen varastotapahtuman tilan perusteella. Valitse yksi seuraavista:
        - *Tilauksessa* – kun tilana on *Tapahtumassa*, tilaus lähettää vastakirjauspyynnön, kun se luodaan. Vastakirjauksen määrä on luodun tilauksen määrä.
        - *Varaus* – Kun tilana on *Varaa tilattu tapahtuma*, tilaus lähettää vastakirjauspyynnön, kun tilaus varataan tai poimitaan, kun sen pakkausluettelo kirjataan tai kun se laskutetaan. Pyyntö käynnistetään vain kerran ensimmäisessä vaiheessa, kun mainittu prosessi tapahtuu. Vastakirjauksen määrä on määrä, jossa varastotapahtuman tila muuttui tilasta *Tilauksessa* tilaan *Tilaukseen varattu* (tai myöhempään tilaan) kulloisellakin tilausrivillä.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Varausominaisuuden käyttäminen varaston näkyvyyssovelluksessa

Kun varauksen ohjelmointirajapintaa kutsutaan, järjestelmää merkitsee tiettyjen tavaroiden ja määrien varauksen. Varaushierarkia on määritettävä ja kirjattavien pyyntöjen on vastattava kyseistä varaushierarkiaa. Varauksia voidaan sitten tehdä kutsumalla suoraan varauksen ohjelmointirajapintoja.

### <a name="configure-the-reservation-hierarchy"></a>Varaushierarkian määrittäminen

Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavoin kuin indeksihierarkia varastosaldoa koskevissa kyselyissä.

Varaushierarkia voi poiketa indeksihierarkiasta. Tämä erillisyys antaa mahdollisuuden toteuttaa sellainen luokanhallinta, jossa käyttäjät voivat eritellä dimensiot vaatimukset määrittäviksi tiedoiksi. Tämä puolestaan antaa mahdollisuuden entistä tarkempiin varauksiin.

Alustava varauksen hierarkia määritetään Power Appsissa avaamalla **Määritykset**-sivu ja määrittämällä sitten **Alustavan varauksen hierarkia** -välilehdessä varaushierarkia lisäämällä ja/tai muokkaamalla dimensioita ja niiden hierarkiatasoja.

Alustavan varauksen historian pitäisi sisältää tunnukset `SiteId` ja `LocationId` komponentteina, koska ne muodostavat osionmäärityksen.

Lisätietoja varausten määrittämisestä: [Varausten määritys](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Varauksen ohjelmointirajapinnan kutsuminen

Varauksia tehdään varaston näkyvyyspalvelussa lähettämällä POST-pyyntö palvelun URL-osoitteeseen, joka voi olla esimerkiksi `/api/environment/{environment-ID}/onhand/reserve`.

Varauspyynnön tekstiosan on sisällettävä organisaation tunnus, tuotetunnus, varatut määrät ja dimensiot: Pyyntö luo yksilöivän varaustunnuksen kullekin varaustietueelle. Varaustietue sisältää yksilöivän tuotetunnus- ja dimensioyhdistelmän.

Kun kutsut varausten ohjelmointirajapintaa, voit ohjata varausten vahvistamista määrittämällä `ifCheckAvailForReserv`-totuusarvoparametrin pyynnön tekstiosassa. `True`-arvo tarkoittaa, että vahvistus vaaditaan, ja `False`-arvo, että vahvistusta ei vaadita. Oletusarvona on `True`.

Jos haluat perua varauksen tai poistaa tiettyjen varastomäärien varauksen, määritä määräsi negatiivinen arvo ja ohita vahvistus määrittämällä `ifCheckAvailForReserv`-parametrin arvoksi `False`.

Esimerkki pyynnön tekstiosasta:

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Varausten vastakirjaus Supply Chain Managementissa

Jos varastotapahtuman tilat sisältävät määritetyn varauksen vastakirjausmääreen, tapahtuman päivitys luo vastakirjauksen vastaavalle varaustietueelle, kun kaikki seuraavat ehdot täyttyvät:

- Varastotapahtuman varaustunnus vastaa varaston näkyvyyspalvelussa olevaa varaustietueen varaustunnusta.
- Varastotapahtuman dimensiot ovat täsmälleen samat kuin varaston näkyvyyspalvelussa olevat varaustietueen dimensiot.
- Varastotapahtuman tilan muutokset käynnistävät varausten vastakirjauksen, kun varastotapahtuman tila ilmaisee, että tilausprosessi on valmistunut tai se on ohitettu.

Vastakirjausmäärä on varastotapahtumissa määritetyn varastomäärän mukainen. Vastakirjaus ei toteudu, jos varattu määrä jää varaston näkyvyyspalveluun.

### <a name="set-up-the-reservation-offset-modifier"></a>Varauksen vastakirjauksen määreen määrittäminen

Jos et ole vielä määrittänyt varausta, määritä varausmuuttuja kohdassa [Määritysominaisuuden käyttöönotto ja määritys](#turn-on) kuvatulla tavalla.

### <a name="set-up-reservation-ids"></a>Varaustunnusten määrittäminen

Varaustunnus yksilöi varaustietueen varaston näkyvyyssovelluksessa. Käyttäjät merkitsevät varaukset Supply Chain Managementissa tilausriveille ilmaisemaan vastaavan varaustietueen vastakirjauksen.

Varaustunnukset määritetään Supply Chain Managementissa seuraavasti:

1. Avaa myyntitilaus (esimerkiksi **Kaikki myyntitilaukset** -sivulla).
1. Valitse **Myyntitilausrivit**-pikavälilehdessä tilausrivi.
1. Valitse **Myyntitilausrivit**-pikavälilehden työkalurivillä **Päivitä rivi \> Varasto \> Varaston näkyvyyden integrointi**.
1. Anna soveltuvat varaustunnukset.

Varaston tila muuttuu vastakirjaukseen määreen määrityksiä vastaavaksi.
