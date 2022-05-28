---
title: Ostotilausten hyväksyminen ja vahvistaminen
description: Tässä ohjeaiheessa käsitellään ostotilauksen tilat, jotka se läpäisee luonnin jälkeen, ja muutoksenhallinnan käyttöönoton vaikutuksen ostotilauksiin.
author: GalynaFedorova
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d38a486c604dc761dcaf12b839d8b9b89b5e0414
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676999"
---
# <a name="approve-and-confirm-purchase-orders"></a>Ostotilausten hyväksyminen ja vahvistaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ostotilauksen tilat, jotka se läpäisee luonnin jälkeen, ja muutoksenhallinnan käyttöönoton vaikutuksen ostotilauksiin.

Kun ostotilaus on luotu, sen on ehkä läpäistävä hyväksyntäprosessi. Kun toimittaja on hyväksynyt tilauksen, ostotilauksen tilaksi määritetään **Vahvistettu**.

## <a name="approval-of-purchase-orders"></a>Ostotilausten hyväksyntä
Jos ostotilauksessa ei käytetä muutoksenhallintaa, sen tila on **Hyväksytty** heti, kun ne on luotu, kun taas muutoksenhallintaa käyttävien ostotilausten tila on **Luonnos**. Ostotilauksen, joka on luotu suunnittelun tilauksen päätilauksesta, tilaksi on aina määritetty **Hyväksytty** muutoksenhallinnan asetuksista riippumatta. Ostotilaus luo varastotapahtumia vain, kun se siirtyy **Hyväksytty**-tilaan. Tämän vuoksi varasto ei näytä olevan varattavissa tai merkittävissä, ennen kuin tilaus on hyväksytty.

Ostotilauksen muutoksenhallinta otetaan käyttöön määrittämällä **Ota muutostenhallinta käyttöön** -vaihtoehto **Hankintaparametrit**-sivulla. Kun muutoksenhallinta on otettu käyttöön, ostotilauksen on läpäistävä hyväksyntätyönkulku ennen valmistumista. Supply Chain Managementissa on työnprosessin editori, jossa voit määrittää työnkulun omaa hyväksyntäprosessiasi vastaavaksi. Tämä työnkulku voi sisältää automaattisen hyväksymisen sääntöjä, sääntöjä, joilla määritetään tiettyjen ostotilausten hyväksyjä, ja pitkään hyväksymistä odottaneen työnkulun eskalointisäännöt. Voit ottaa muutoksenhallintaprosessin käyttöön kaikille toimittajille tai tietyille toimittajille. Voit myös määrittää prosessin niin, että se voidaan ohittaa yksittäisissä ostotilauksissa.

Kun muutoksenhallinta on otettu käyttöön, ostotilaukset läpäisevät kuusi hyväksyntätilaa **Luonnos**-tilasta **Päätetty**-tilaan. Kun tilaus on hyväksytty, sitä muokkaavien käyttäjien on käytettävä **Pyydä muutosta** -toimintoa.

| Hyväksynnän tila | Kuvaus                                                                      | Muutoksen pyyntö on otettu käyttöön |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Luonnos           | Ostotilaus on luonnos eikä sitä ole lähetetty hyväksyttäväksi ostotilauksen työnkulkuun.     | Ei                        |
| Tarkistuksessa       | Ostotilaus lähetettiin hyväksyttäväksi ostotilauksen työnkulkuun. Hyväksyntää odotetaan.       | Ei                        |
| Hylätty        | Ostotilaus hylättiin hyväksymisprosessin aikana.                                 | Ei                        |
| Hyväksytty        | Ostotilaus hyväksyttiin.                                                             | Kyllä                       |
| Vahvistettu       | Ostotilaus vahvistettiin. Ostotilausta ei voi vahvistaa, ennen kuin se on hyväksytty.        | Kyllä                       |
| Päätetty       | Ostotilaus on lopullinen. Se on nyt rahoituksellisesti suljettu eikä sitä voi enää muuttaa. | Ei                        |

## <a name="confirming-purchase-orders"></a>Ostotilausten vahvistaminen
Ostotilausten, joiden hyväksyntätila on **Hyväksytty**, on ehkä läpäistävä lisävaiheita ennen vahvistusta. Toimittajalle on ehkä esimerkiksi lähetettävä hintoja, alennuksia tai toimituspäiviä koskeva kysely. Tässä tapauksessa voit määrittää ostotilauksen tilaksi **Ulkoisessa tarkistuksessa** **Ostokysely**-toiminnolla.

Toimittajaportaalin käyttöoikeudet omaavat toimittajat voivat tarkastella tilauksia portaalissa ja joko hyväksyä tai hylätä ne. Tämän tarkistusprosessin aikana ostotilauksen tila on **Ulkoisessa tarkistuksessa**. Toimittajaportaali voidaan määrittää siten, että toimittaja vahvistaa tilauksen automaattisesti Supply Chain Managementissa. Voit vaihtoehtoisesti vahvistaa tilauksen manuaalisesti, kun on saanut vahvistuksen toimittajalta. Jos toimittaja hylkää ostotilauksen, hylkäyksen lisäksi toimitetaan hylkäyksen syy ja muutosehdotukset. Tässä tapauksessa ostotilauksen tilaksi jää **Ulkoisessa tarkistuksessa**.

Lisäksi käytettävissä on vaihtoehto, jolla tilaukselle voi luoda proforma-vahvistuksen ennen varsinaisen vahvistuksen käsittelyä. Tällä vaihtoehdolla vain luodaan raportti, jonka voit jakaa toimittajan kanssa. Sillä ei luoda kirjauskansiotietoja.

Kun toimittaja on hyväksynyt tilauksen, seuraavana vaiheena on ostotilauksen kirjaaminen vahvistetuksi. Voit tehdä tämän vaiheen joko **Vahvistus**- tai **Vahvista**-toiminnolla. Kumpikin toiminto määrittää tilauksen hyväksyntätilaksi **Vahvistettu**. Tilauksen vahvistus käynnistää kaksi lisäprosessia:

-   Kirjauskansio luodaan tallentamaan tarkka kopio siitä, mikä vahvistettiin järjestelmässä. Joskus tilauksiin on tehtävä muutoksia ja lisäkirjauskansiot luodaan, kun päivitetty tilaus on vahvistettu. Voit tarkastella näiden kirjauskansioiden avulla vahvistetun tilauksen eri versioita.
-   Kirjanpidolliset jaot on luodaan ja tilaus- ja budjettitarkistuksia tehdään, jos tämä toiminto on otettu käyttöön. Jos jompikumpi tarkistus epäonnistuu, avautuva virhesanoma ilmoittaa, että ostotilaukseen on tehtävä muutoksia, ennen kuin se voidaan vahvistaa uudelleen.

Toimittaja voi pyytää jonkinlaisen vakuuden siitä, että osto maksetaan. Ostoreskontraprosessissa on erilaisia tapoja, jolla tämä takuu voidaan antaa. Esimerkiksi **Ennakkomaksu**-toiminto varaa varat ostotilaukseen ja tämä ennakkomaksu tallennetaan ostotilaukseen.

## <a name="changing-purchase-orders"></a>Ostotilausten muuttaminen
Joissakin tilanteissa ostotilausta on muutettava, ennen kuin sen hyväksynnän tilana on **Hyväksytty** tai **Vahvistettu**.

Jos ostotilaus luotiin muutoksenhallintaprosessilla, voit tehdä muutoksia peruuttamalla tilauksen tai, jos tilaus on jo hyväksytty, **Pyydä muutosta** -toiminnolla. Tässä tapauksessa hyväksynnän tilaksi vaihdetaan **Luonnos**, ja voit sitten muokata tilausta. Kun muutokset ovat valmiina, ostotilaus on ehkä lähetettävä uudelleenhyväksyttäväksi. Voit määrittää uudelleenhyväksyntää edellyttävät muutostyypit käyttämällä **Ostotilausten uudelleenhyväksymissääntö** -käytäntösääntöä **Ostokäytännöt**-sivulla.

Jos osa ostotilausrivin tilatusta määrästä on toimitettu, tilattua määrää ei voi muuttaa, kun ostotilaus on **Luonnos**-tilassa. Voit kuitenkin muuttaa **toimituksen jäännös** -määrää ostotilauksen rivillä, joka on **luonnos**-tilassa.

Kun tilaus on vahvistettu, et voi enää poistaa sitä. Voit kuitenkin peruuttaa tilauksen koko määrän tai minkä tahansa jäljellä olevan määrän, kunhan määrää ei ole vastaanotettu tai laskutettu. Voit sitten estää lisäkäsittelyn **Viimeistele**-toiminnolla. 


## <a name="canceling-purchase-orders"></a>Ostotilausten peruuttaminen

Ostotilaus voidaan peruuttaa käyttämällä otsikon **Peruuta**-toimintoa.

Jos määrä on osittain rekisteröity, vastaanotettu tai laskutettu, voit peruuttaa vain sen osan määrästä, jota ei ole rekisteröity, vastaanotettu tai laskutettu. Tällöin tilausmäärää vähennetään vastaavasti. Kun rivin määrä päivitetään, päivitetään myös rivin tila. Esimerkki: rivin alkuperäinen määrä on 5 ja 3 otetaan vastaan. Tällöin vain kaksi voidaan peruuttaa. Tämän jälkeen rivin tilaksi vaihdetaan **Vastaanotettu**.

Jos jäljellä oleva toimitus lisätään tilausriville ja se ylittää tilausrivin määrän, **Peruuta**-toiminto ei peruuta liiallista määrää. Sen sijaan rivi pysyy tilassa **Avoin tilaus**, koska sillä on määrää jäljellä. Esimerkki: rivin alkuperäinen määrä on 5 ja jäljellä oleva toimitus on 7. Jos tilaus peruutetaan, viisi peruutetaan ja määrä 2 jää jäljelle, kuten varastotapahtumista ilmenee.

Jos haluat peruuttaa ostotilausrivin koko määrän, sinun on peruutettava rivin jäljellä oleva toimitus. Tämän jälkeen rivin tilaksi päivitetään **Peruutettu**.

Jos ostotilaus on muutostenhallinnan piirissä, mikä tahansa muutos, kuten tilauksen tai jäljellä olevan toimituksen peruutus, on ilmoitettava työnkulkujärjestelmälle ja hyväksyttävä, ennen kuin prosessi voidaan suorittaa loppuun ja varastotapahtumien tilaksi päivittää peruutettu.

## <a name="additional-resources"></a>Lisäresurssit

[Ostotilausten yleiskatsaus](purchase-order-overview.md)

[Ostotilausten luominen](purchase-order-creation.md)

[Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)

[Toimittajan laskujen yleiskatsaus](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]