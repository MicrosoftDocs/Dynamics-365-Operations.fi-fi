---
title: Toimenpidesanomat
description: Toimintosanoma on järjestelmän luoma ehdotus olemassa olevan suunnitellun tai vahvistetun tilauksen muuttamisesta.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570251"
---
# <a name="action-messages"></a>Toimenpidesanomat

[!include [banner](../includes/banner.md)]

Toimintosanoma on järjestelmän luoma ehdotus olemassa olevan suunnitellun, hyväksytyn tai vahvistetun tilauksen muuttamisesta.

Pääsuunnittelulaskenta luo toimintosanomat vaatimusten muuttuessa. Esimerkiksi lähetyspäivä tai määrä on muuttunut myyntitilauksessa, kun olet jo luonut ostotilauksen kysynnän täyttämistä varten. Siinä tapauksessa pääsuunnittelun laskenta luo vähintään yhden toimintosanoman, joka ehdottaa ostotilauksen päivittämistä. Voit päättää, tehdäänkö ehdotetut muutokset.

Voit määrittää, millä tavalla toimintosanomat lasketaan nimikkeeseen liitettävälle kattavuusryhmälle.

## <a name="select-action-messages"></a>Toimintosanomien valitseminen

Voit valita **Kattavuusryhmät**-sivulla toimintosanomat, jotka haluat järjestelmän muodostavan sekä kattavuusryhmät tai nimikkeet, joita sanomat koskevat. Seuraavassa taulukossa luetellaan valittavissa olevat toimintosanomat.

| Sanoma | Kuvaus |
|---|---|
| Aikaista | Järjestelmä luo tarvittaessa toimintosanomat, joilla tilaukset siirretään aikaisemmaksi. Voit määrittää **Aikaistamisen aikaraja** -kentässä kuinka monta päivää vastaanoton ja varasto-oton välillä voi enintään kulua ilman aikaistamistoimintoa. |
| Lykkää | Järjestelmä luo tarvittaessa toimintosanomat, joilla tilaukset siirretään myöhemmäksi. Voit määrittää **Lykkäyksen aikaraja** -kentässä kuinka monta päivää vastaanoton ja varasto-oton välillä voi enintään kulua ilman lykkäystoimintoa. |
| Vähennä määrää | Järjestelmä luo toimintosanomia, kun tuotantotilausten, ostotilausten ja muiden vastaanottotilausten määrän pitäisi pienentyä, jotta varastotasot eivät ylittyisi. |
| Lisää määrää | Järjestelmä luo toimintosanomia, kun tuotantotilausten, ostotilausten ja muiden vastaanottotilausten määrän pitäisi kasvaa varastopulan ehkäisemiseksi. |
| Johdetut toimenpiteet | Vastaanottotapahtumista luodut toimenpidesanomat siirretään kaikkiin johdettuihin vaatimuksiin, ja nämä vaatimukset täyttävät vastaanottotapahtumat luodaan tarvittavat toimenpidesanomat. |

Seuraavissa osissa on muutamia yksityiskohtaisia skenaarioita.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Toimenpiteiden lisääminen ja vähentäminen tuotteen oletustilausmäärissä

Nimikkeen **oletustilausasetukset**-sivulla voit määrittää vähimmäistilauksen määrän, tilauksen enimmäismäärän ja useita arvoja. Järjestelmä ottaa sitten nämä asetukset huomioon toimenpiteitä ehdottaessaan, jotta ehdotukset eivät koskaan aiheuta alitarjontaa.

Esimerkiksi nimikkeen **oletustilausasetukset**-sivulla on seuraavat asetukset:

- **Tilauksen vähimmäismäärä:** *0*
- **Tilauksen enimmäismäärä:** *90*
- **Kerrannainen:** *20*

Jos kysyntää on 60 nimikkeelle, pääsuunnittelu luo suunnitellun ostotilauksen määrälle 60. Jos kysyntää lisätään 30:llä, pääsuunnittelu ehdottaa 40:n korotusta, koska se perustuu 20:n kerrannaisiin eikä koskaan aiheuta alitarjontaa.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Varmuusvarastoon liittyvien tilausten toimintosanomat

Toimisanomat tilauksille, joissa toimitusten varmuusvarasto ei koskaan ehdota huollon määrän pienentämistä varmuusvarastossa tarvittavan määrän alapuolelle. Toisin sanoen jos tilaus toimittaa turvallisuusvarastoa ja asiakkaiden kysyntää ja kysyntä pienenee tai peruutetaan, pääsuunnittelu ehdottaa suunnitellun tilauksen pienentämistä vähentyneellä kysynnällä. Se ei kuitenkaan koskaan ehdota arvoa, joka on pienempi kuin tarvittava varmuusvarasto.

Järjestelmä ei ehdota varmuusvaraston toimitusten lykkäämistoimia, koska oletettavasti varmuusvarasto on toimitettava tarvittavana aikana ja vaadittuna päivämääränä.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Tuoterakenteita koskevat ennakko- ja viivästystoiminnot

Tuoterakenteiden komponentteihin liittyvät toimenpiteet on otettava käyttöön ennen päänimikkeiden toimintoja, koska tämä saattaa vaikuttaa ylemmän tason tuoterakenteiseen liittyviin lisätilauksiin. Suorita sitten pääsuunnittelu uudelleen, jotta voit laskea uudelleen ja ehdottaa asianmukaisia toimenpiteitä.

Kyse voi olla esimerkiksi seuraavasta tilanteesta.

- Tyypin *Tuotanto* lopputuotteella *FG* on tuoteluettelo, joka sisältää raaka-aineen *RM*.
- Tämän päivän päivämäärä on 21. tammikuuta.
- Aiemmin luotu, julkaistu tuotantotilaus tuotteelle *FG* on ajoitettu 25. tammikuuta.
- Olemassa olevan tuotantotilauksen tukemiseksi yleissuunnittelu on luonut suunnitellun ostotilauksen tarvittavalle raaka-aineelle *RM*. Tilauksen tarvepäivä on 25.1.
- *FG*:lle luodaan tänään uusi myyntitilaus. Sen tarvepäivämäärä on kuluva päivä (21. tammikuuta).
- 21. tammikuuta on suljettu toimitusta varten *RM*-kalenterissa, mutta 22. tammikuuta on avoinna.

Kun pääsuunnittelu suoritetaan, se luo toimenpidesanomia, jotka ehdottavat aiemmin ajoitetun tuotannon jatkamista, jotta voit täyttää tämän päivän tilauksen.

- Vastatakseen uuteen kysyntään se ehdottaa *FG*:n tuotantotilauksen siirtämistä tammikuun 21. päivään. (Se tekee tämän ehdotuksen ottamatta huomioon *RM*:n sulkupäivämäärää.)
- Koska *RM* vaaditaan edelleen tuotantotilaukselle, se ehdottaa siirtämistä ylöspäin myös suunnitellussa ostotilauksessa. Tällä kertaa se kuitenkin tarkistaa *RM*-kalenterin. Siksi se ehdottaa, että suunniteltu *RM*-ostotilaus siirretään 22. tammikuuta (koska tammikuun 21. päivä on suljettu).

Kuten näet, tarvittava raaka-aine *RM* saapuu nyt liian myöhään *FG*:n ajoitettuun tuotantoon. Siksi sinun on ensin sovellettava ennakkotoimintoa suunniteltuun ostotilaukseen *RM* ja suoritettava sitten yleissuunnittelu uudelleen. Siinä vaiheessa yleissuunnittelu luo uuden toimintoviestin, joka ehdottaa *FG*:n tuotantotilauksen siirtämistä tammikuun 22. päivään.
