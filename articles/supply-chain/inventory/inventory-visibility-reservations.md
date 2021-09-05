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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345146"
---
# <a name="inventory-visibility-reservations"></a>Varaston näkyvyyden varaukset

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tässä aiheessa käsitellään varausominaisuuden määrittämistä luomaan varauksia, käyttämään varauksia ja/tai poistamaan määritettyjen varastomäärien varauksia varaston näkyvyyssovelluksella.

Varauksilla merkitään varastomäärä, joka käytetään myöhemmin. Varausta luotaessa järjestelmä estää muita tilauksia varaamasta tai käyttämästä varattuja tavaroita siihen saakka, että varaus joko käytetään tai varaus poistetaan. Varaukset luodaan, niitä käytetään ja ne peruutetaan käyttämällä ohjelmointirajapintakutsuja varaston näkyvyyspalveluun.

Microsoft Dynamics 365 Supply Chain Management (ja muut kolmannen osapuolen järjestelmät) voidaan lisäksi määrittää tekemään vastakirjaus varatulle määrälle varaston näkyvyyssovelluksen avulla. Vastakirjausmäärä poistetaan varaustietueista varaston näkyvyyssovelluksessa.

Kun varaustoiminto otetaan käyttöön, Supply Chain Management on automaattisesti valmis tekemään vastakirjaus varauksille, jotka tehdä varaston näkyvyyssovelluksella.

> [!NOTE]
> Vastakirjaustoimintoa varten tarvitaan Supply Chain Management 10.0.22 tai uudempi versio. Jos varaston näkyvyyssovelluksen varauksia halutaan käyttää, kannattaa odottaa siihen saakka, että Supply Chain Management on päivitetty vähintään versioon 10.0.22.

## <a name="turn-on-the-reservation-feature"></a>Varausominaisuuden ottaminen käyttöön

Varausominaisuus otetaan käyttöön seuraavasti:

1. Avaa **Varaston näkyvyys** Power Appsissa.
1. Avaa **Määritykset**-sivu.
1. Ota *OnHandReservation*-ominaisuus käyttöön **Ominaisuuksien hallinta** -välilehdessä.
1. Kirjaudu Supply Chain Managementiin.
1. Valitse **Varastonhallinta \> Asetukset \> Varaston näkyvyyden integroinnin parametrit**.
1. Määritä **Varaston vastakirjaus** -kohdassa **Ota varaston vastakirjaus käyttöön** -asetukseksi *Kyllä*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Varausominaisuuden käyttäminen varaston näkyvyyssovelluksessa

Kun varauksen ohjelmointirajapintaa kutsutaan, järjestelmää merkitsee tiettyjen tavaroiden ja määrien varauksen. Varaushierarkia on määritettävä ja kirjattavien pyyntöjen on vastattava kyseistä varaushierarkiaa. Varauksia voidaan sitten tehdä kutsumalla suoraan varauksen ohjelmointirajapintoja.

### <a name="configure-the-reservation-hierarchy"></a>Varaushierarkian määrittäminen

Varaushierarkia ilmaisee dimensiojärjestyksen, joka on määritettävä varauksia tehtäessä. Se toimii samalla tavoin kuin indeksihierarkia varastosaldoa koskevissa kyselyissä.

Varaushierarkia voi poiketa indeksihierarkiasta. Tämä erillisyys antaa mahdollisuuden toteuttaa sellainen luokanhallinta, jossa käyttäjät voivat eritellä dimensiot vaatimukset määrittäviksi tiedoiksi. Tämä puolestaan antaa mahdollisuuden entistä tarkempiin varauksiin.

Alustava varauksen hierarkia määritetään Power Appsissa avaamalla **Määritykset**-sivu ja määrittämällä sitten **Alustavan varauksen yhdistämismääritys** -välilehdessä varaushierarkia lisäämällä ja/tai muokkaamalla dimensioita ja niiden hierarkiatasoja.

### <a name="call-the-reservation-api"></a>Varauksen ohjelmointirajapinnan kutsuminen

Varauksia tehdään varaston näkyvyyspalvelussa lähettämällä POST-pyyntö palvelun URL-osoitteeseen, joka voi olla esimerkiksi `/api/environment/{environment-ID}/onhand/reserve`.

Varauspyynnön tekstiosan on sisällettävä organisaation tunnus, tuotetunnus, varatut määrät ja dimensiot: Pyyntö luo yksilöivän varaustunnuksen kullekin varaustietueelle. Varaustietue sisältää yksilöivän tuotetunnus- ja dimensioyhdistelmän.

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

> [!NOTE]
> Vastakirjaustoiminto on saatavana versiosta 10.0.22 alkaen

### <a name="set-up-the-reserve-offset-modifier"></a>Varauksen vastakirjauksen määreen määrittäminen

Varauksen vastauskirjauksen määrää määrittää tilauksen vastakirjaukset käynnistävän käsittelyvaiheen. Vaihetta seurataan tilauksen varastotapahtuman tilan perusteella. Varauksen vastakirjauksen määre määritetään seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Varaston näkyvyyden integroinnin parametrit \> Varauksen vastakirjaus**.
1. Määritä **Varauksen vastakirjauksen määrä** -kentän arvoksi jokin seuraavista arvoista:

    - *Tilauksessa* – kun tilana on *Tapahtumassa*, tilaus lähettää vastakirjauspyynnön, kun se luodaan.
    - *Varaus* – Kun tilana on *Varaa tilattu tapahtuma*, tilaus lähettää vastakirjauspyynnön, kun tilaus varataan tai poimitaan, kun sen pakkausluettelo kirjataan tai kun se laskutetaan. Pyyntö käynnistetään vain kerran ensimmäisessä vaiheessa, kun mainittu prosessi tapahtuu.

### <a name="set-up-reservation-ids"></a>Varaustunnusten määrittäminen

Varaustunnus yksilöi varaustietueen varaston näkyvyyssovelluksessa. Käyttäjät merkitsevät varaukset Supply Chain Managementissa tilausriveille ilmaisemaan vastaavan varaustietueen vastakirjauksen.

Varaustunnukset määritetään Supply Chain Managementissa seuraavasti:

1. Avaa myyntitilaus (esimerkiksi **Kaikki myyntitilaukset** -sivulla).
1. Valitse **Myyntitilausrivit**-pikavälilehdessä tilausrivi.
1. Valitse **Myyntitilausrivit**-pikavälilehden työkalurivillä **Päivitä rivi \> Varasto \> Varaston näkyvyyden integrointi**.
1. Anna soveltuvat varaustunnukset.

Varaston tila muuttuu vastakirjaukseen määreen määrityksiä vastaavaksi.
