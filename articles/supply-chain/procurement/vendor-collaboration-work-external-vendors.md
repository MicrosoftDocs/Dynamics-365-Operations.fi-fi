---
title: Toimittajayhteistyö ulkoisten toimittajien kanssa
description: Tässä artikkelissa selitetään, miten ostoedustajat voivat tehdä yhteistyötä ulkoisten toimittajien kanssa sekä vaihtaa ostotilauksia ja tavaralähetysvarastoa koskevia tietoja.
author: GalynaFedorova
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 25561802996514f6f60fc9400c22dc61a30ef1c8
ms.sourcegitcommit: bad64015da0c96a6b5d81e389708281406021d4f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023785"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Toimittajayhteistyö ulkoisten toimittajien kanssa

[!include [banner](../includes/banner.md)]

**Toimittajayhteistyö**-moduuli on tarkoitettu toimittajille, joilla ei ole sähköisten tietojen vaihdon (EDI) Microsoft Dynamics 365 Supply Chain Management -integrointia. Toimittajat voivat käsitellä siinä ostotilauksia, laskuja, tavaralähetysvaraston tietoja ja tarjouspyyntöjä. Lisäksi he voivat käyttää joitakin osia toimittajan päätiedoista. Tässä artikkelissa selitetään, miten voit tehdä yhteistyötä ulkoisten toimittajien kanssa, jotka käsittelevät toimittajayhteistyöliittymässä ostotilauksia, tarjouspyyntöjä ja tavaralähetysvarastoja. Siinä selitetään myös, miten toimittajayhteistyö voidaan ottaa käyttöön tietylle toimittajalle ja miten kaikkien määritetään tiedot, jotka kaikki toimittajat näkevät, kun he vastaavat ostotilaukseen.

Lisätietoja siitä, mitä ulkoiset toimittajat voivat tehdä toimittajan toimittajayhteistyöliittymällä, on kohdassa [Toimittajayhteistyö asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md).

Lisätietoja siitä, kuinka toimittajat voivat käyttää toimittajayhteistyötä laskutusprosesseissa, on kohdassa [Toimittajayhteistyön laskutustyötila](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). Tietoja siitä, miten uusia toimittajayhteistyön käyttäjiä voidaan valmistella, on kohdassa [Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Ostotilaukseen vastaaville toimittajille näytettävien tietojen määrittäminen

Kun toimittajat vastaavat lähettämääsi ostotilaukseen, he näkevät jonkin kolmesta sanomaruudusta, jossa heidän on vahvistettava ostotilauksen hyväksyntä, hylkääminen tai hyväksyminen muutosten kera. Koska tässä vaiheessa toimittajalle näytettävät tiedot voivat olla yrityskohtaisia, voit määrittää tekstin, joka näkyy jokaisessa vahvistussanomassa. Teksti voi esimerkiksi ilmoittaa toimittajalle tietoja prosessin seuraavista vaiheista tai noudatettavista ehdoista.

Ostotilauksen vastauksessa näkyvän tekstin määritysvaiheet

1. Valitse **Ostotilauksiin vastaaville toimittajille tarkoitetut tiedot** -sivulla ensin vastauksen tyyppi ja sitten **Muokkaa**.
2. Anna **Tietosanoma**-ruudussa sanomaruudussa toimittajille näytettävät tiedot.

Jos sanomat on lisättävä useammalla kielellä, luo erilliset sanomat ja määritä kullekin tarvittava kielikoodi. Viesti näytetään kullekin toimittajalle tämän käyttämällä kielellä.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Toimittajayhteistyön asetusten määrittäminen tietylle toimittajalle

Järjestelmänvalvoja määrittää toimittajayhteistyön yleiset asetukset, kuten käyttöoikeusroolit, jotka kaikilla kanssasi yhteistyötä tekevillä toimittajilla on. On kuitenkin myös joitakin toimittajatilikohtaisia asetuksia. Sinun onkin määritettävä nämä asetukset.

- Toimittajayhteistyön käyttöönotto.
- Määritä, näkeekö toimittaja hintatiedot.

### <a name="enabling-vendor-collaboration"></a>Toimittajayhteistyön ottaminen käyttöön

Ennen käyttäjätilien luontia ulkoiselle toimittajalle on määritettävä toimittajatili, jotta toimittaja voi käyttää toimittajayhteistyötä. Määritä **Toimittajat**-sivun **Yleinen**-välilehdessä **Yhteistyön aktivointi**-kenttä. Käytettävissä ovat seuraavat asetukset:

- **Aktiivinen (ostotilaus vahvistetaan automaattisesti)**– ostotilaukset vahvistetaan automaattisesti, jos toimittaja hyväksyy sen ilman muutoksia. Jos käytät tätä vaihtoehtoa, varmista, että ajoitat *Vahvista hyväksytyt ostotilaukset toimittajayhteistyöstä* -erätyön. Se on vastuussa vahvistusten käsittelemisestä. Lisätietoja on seuraavassa osassa.
- **Aktiivinen (ostotilausta ei vahvisteta automaattisesti)**– organisaation on vahvistettava ostotilaukset manuaalisesti, kun toimittaja on hyväksynyt ne.

### <a name="scheduling-the-auto-confirmation-batch-job"></a>Automaattisen vahvistuksen erätyön ajoittaminen

Jos käytät yhdellä tai usealla toimittajalla **Aktiivinen (ostotilaus vahvistetaan automaattisesti)** -vaihtoehtoa (kuten edellisessä osassa on kerrottu), ajoita *Vahvista hyväksytyt ostotilaukset toimittajayhteistyöstä* -erätyö, joka on vastuussa ostotilausten käsittelemisestä ja vahvistamisesta. Muussa tapauksessa automaattisia vahvistuksia ei tehdä koskaan. Ajoita tämä työ seuraavien ohjeiden mukaan.

1. Siirry kohtaan **Hankinta \> Ostotilaukset \> Ostotilauksen vahvistus \> Vahvista hyväksytyt ostotilaukset toimittajayhteistyöstä**.
1. Valitse **Vahvista hyväksytyt ostotilaukset toimittajayhteistyöstä** -valintaikkunassa **Suorita taustalla** -pikavälilehdessä **Toistuminen**.
1. Määritä **Määritä toistuvuus** -valintaikkunassa työn suoritusaikataulu. Kun valitset aikataulun, ota huomioon seuraavat seikat:

    - Jos järjestelmä käsittelee suuria tietomääriä ja suorittaa useita erätöitä, suorituskyky saattaa huonontua. Tässä tapauksessa työtä ei todennäköisesti kannata ajaa useammin kuin 10 minuutin välein (muista vaatimuksista riippuen). Jos suorituskyky ei huonone, voit suorittaa työn jopa 1-2 minuutin välein tarvittaessa.
    - Jos toimittaja toimittaa tavarat yleensä nopeasti (lupaamansa päivän aikana), työ voidaan määrittää toistuvaksi (10–30 minuutin välein). Tällöin varastotyöntekijät voivat vastaanottaa tavarat vahvistettua ostotilausta vastaan vahvistuksen jälkeen.
    - Jos toimittajalla on pitkä toimitusaika (yli 24 tuntia), voit määrittää tämän tehtävän suoritettavaksi vain esimerkiksi kerran päivässä.

1. Valitse **OK**, jos haluat käyttää aikataulua ja palata **Vahvista hyväksytyt ostotilaukset toimittajayhteistyöstä** -valintaikkunaan.
1. Määritä tarvittavat tausta-asetukset. Valintaikkunassa ovat normaalit vaihtoehdot Supply Chain Managementin erätöiden määrittämistä varten.

Lisätietoja erätöistä on kohdassa [Eräkäsittelyn yleiskatsaus](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Hintatietojen näkyvyyden määrittäminen toimittajille

Voit jakaa ostotilausten hintatiedot toimittajayhteistyöliittymässä valitsemalla **Ostotilauksen hinnat/summa** -asetukseksi **Kyllä** toimittajatilin **Oletusostotilaukset**-välilehdessä. Nämä hintatiedot sisältävät yksikköhinnan, alennukset ja kulut.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Ostotilausten käsitteleminen toimittajayhteistyön ollessa käytössä

### <a name="sending-a-po-to-a-vendor"></a>Ostotilauksen lähettäminen toimittajalle

Ostotilaukset laaditaan Supply Chain Managementissa. Kun ostotilauksen tilana on **Hyväksytty**, se lähetetään toimittajalle valitsemalla **Ostotilaus**-sivulla **Lähetä vahvistettavaksi**. Ostotilauksen tila tulee sitten **Ulkoisessa tarkistuksessa**. Kun ostotilaus on lähetetty, toimittaja näkee sen **Tarkistettavat ostotilaukset** -sivulla toimittajayhteistyöliittymässä. Toimittaja voi hyväksyä ostotilauksen, hylätä sen tai ehdottaa siihen muutoksia. Toimittaja voi myös lisätä esimerkiksi ostotilaukseen tehtäviä muutoksia koskevia kommentteja. Jos haluat kiinnittää toimittajan huomion uuteen ostotilaukseen, voit myös lähettää ostotilauksen sähköpostitse tulostuksenhallintajärjestelmässä.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Toimittajan tekemä ostotilauksen hyväksyntä ja vahvistaminen

Kun toimittaja on hyväksynyt ostotilauksen, ostotilaus voidaan vahvistaa automaattisesti tai se on vahvistettava manuaalisesti. Toiminta määräytyy sen mukaan se, onko **Yhteistyön aktivointi** -kentän asetukseksi valittu toimittajalle **Aktiivinen (ostotilaus vahvistetaan automaattisesti)** vai **Aktiivinen (ostotilausta ei vahvisteta automaattisesti)**.

Seuraavassa taulukossa on tyypillinen tietojen vaihto sen mukaan, miten toimittaja vastaa, kun hänelle lähetetään ostotilaus vahvistettavaksi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Toimittajan vastaus</th>
<th>Tulos</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Toimittaja <strong>hyväksyy</strong> tilauksen ja Supply Chain Management on määritetty vahvistamaan automaattisesti toimittajan hyväksymät ostotilaukset.</td>
<td>Tilauksen tilaksi päivitetään <strong>Vahvistettu</strong> . Jos tilausta ei voi jostain syystä päivittää, toimittajan vastaukseksi kirjataan silti <strong>Hyväksytty</strong> mutta ostotilauksen tila on edelleen <strong>Ulkoisessa tarkistuksessa</strong>. 

Toimittajalle lähetetyn ostotilauksen, jonka tila on <strong>Ulkoisessa tarkistuksessa</strong>, riveille päivitetään vahvistetut toimituspäivämäärät. Tämä päivitys käynnistää uuden version, joka tilaksi määritetään automaattisesti <strong>Vahvistettu</strong>. Kun ostotilaus on vahvistettu, se näkyy toimittajayhteistyöliittymässä.</td>
</tr>
<tr class="odd">
<td>Toimittaja <strong>hyväksyy</strong> tilauksen, mutta Supply Chain Managementia ei ole määritetty vahvistamaan automaattisesti toimittajan hyväksymiä ostotilauksia.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hyväksytty</strong>, mutta ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan.

Toimittajalle lähetetyn ostotilauksen, jonka tila on <strong>Ulkoisessa tarkistuksessa</strong>, riveille päivitetään vahvistetut toimituspäivämäärät. Tämä päivitys käynnistää uuden version, joka tilaksi määritetään automaattisesti <strong>Ulkoisessa tarkistuksessa</strong>. Voit sitten vahvistaa ostotilauksen manuaalisesti.</td>
</tr>
<tr class="even">
<td>Toimittaja <strong>hylkää</strong> tilauksen.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hylätty</strong>, ja ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan. Hylkäys vastaanotetaan yhdessä toimittajan viestin kanssa.</td>
</tr>
<tr class="odd">
<td>Toimittaja <strong>hyväksyy</strong> tilauksen <strong>muutosten kera</strong>. Muutoksia on ehdotettu rivin tasolla. Toimittaja voi hyväksyä tai hylätä yksittäisiä rivejä. Toimittaja voi ehdottaa myös esimerkiksi seuraavia muutoksia:
<ul>
<li>Päivämäärien tai määrien muuttaminen.</li>
<li>Jaa rivit eri toimituspäivämäärille tai määrille.</li>
<li>Korvaa nimike.</li>
</ul>
Toimittaja ei voi muuttaa hintatietoja ja kuluja. Toimittajan voi kuitenkin ehdottaa niiden muuttamista käyttämällä huomautuksia.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hyväksytty muutosten kera</strong> ja ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan. Tilat näyttävät millaisia muutoksia toimittaja on ehdottanut. Lisätietoja muutosten automaattisesta käytöstä on jäljempänä tämän artikkelin kohdassa &quot;Ostotilauksen päivittäminen toimittajan ehdottaessa muutoksia&quot;. </td>
</tr>
</tbody>
</table>

Voit seurata **Ostotilauksen valmistelu** -työtilan avulla, mihin ostotilaukseen toimittaja on vastannut. Työtilassa on kaksi luetteloa, joissa **Ulkoisessa tarkistuksessa** -tilassa olevat ostotilaukset:

- Ulkoisessa tarkistuksessa -kohde vaatii toiminnon
- Ulkoisessa tarkistuksessa, odottaa toimittajan vastausta

### <a name="changing-a-po"></a>Ostotilauksen muuttaminen

Jos muutat ostotilausta, johon toimittaja on jo vastannut, toimittajalle on lähetettävä ostotilauksen uusi versio. Uuden ostotilausversion loppuliite osoittaa, että kyseessä on aiemmin lähetetyn ostotilauksen muokattu versio. **Ostotilausten toimittajan vahvistushistoria** -sivulla sinä ja toimittajat voitte seurata jokaisen tilauksen historiatietoja. Ostotilauksen aiemmin vahvistettu versio pysyy vahvistettujen tilausten luettelossa, kunnes uusi ostotilaus on vahvistettu.

### <a name="canceling-a-po"></a>Ostotilauksen peruuttaminen

Kun peruutat ostotilauksen, tilaksi vaihtuu **Hyväksytty**. Sinun on lähetettävä ostotilaus takaisin toimittajalle, jotta he voivat vahvistaa tai hylätä peruutuksen. Peruutuksen vahvistuksen jälkeen ostotilaus näkyy toimittajan vahvistettujen ostotilausten luettelossa **Peruutettu**-tilassa.

### <a name="adding-attachments-to-a-po"></a>Liitteiden lisääminen ostotilaukseen

Voit lisätä liitteitä, esimerkiksi tiedostoja, kuvia ja huomautuksia ostotilaukseen käyttämällä tiedostojen hallintajärjestelmää. **Ulkoinen**-tyyppiset liitteet näytetään toimittajalle, kun lähetät ostotilauksen hänelle.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Ostotilauksen päivittäminen toimittajan ehdottaessa muutoksia

Jos toimittaja on vastannut ostotilaukseen ja ehdottanut muutoksia, seuraava vaihe on vastauksen käsitteleminen.

Voit etsiä **Ostotilauksen valmistelu** -työtilan **Ulkoisessa tarkistuksessa -kohde vaatii toiminnon** -luettelosta ostotilaukset, jotka toimittaja on hyväksynyt muutosten kera. Voit siirtyä tästä luettelosta myös toimittajan vastaukseen.

Toimittaja voi muuttaa seuraavat vastauksen otsikon tiedot:
 
- Toimittajan asiakirjan viite
- Toimitustapa
- Toimitusehto
- Vahvistettu toimituspäivämäärä

Toimittaja voi lisätä myös huomautuksen tai liitteen.

Toimittaja voi muuttaa rivillä määrä- ja toimituspäivämäärätiedot, lisätä huomautuksia ja liitteitä, hylätä rivin, korvata rivin toisella tekstinä annettavalla tuotteella sekä jakaa rivin useisiin toimituksiin. Rivin tila vaihtelee toimittajan ehdottamien muutoksen mukaisesti.
    
- **Hyväksytty muutosten kera**
- **Hylätty**
- **Korvattu** – tässä tapauksessa on lisätty ylimääräinen rivi, jonka tila on **Korvaava**.
- **Vahvistettu**
- **Jaa aikatauluksi** – Tässä tapauksessa lisättyjen ylimääräisten rivien tila on **Aikataulun rivit**.

Jos rivillä ei ole muutoksia, rivin tila on **Hyväksytty**.

Vastauksen rivien tilat ilmaisevat toimittajan tekemien muutosten tyypin. Lisäksi kaikki muutetut kentät näkyvät lihavoituna, mikä auttaa havaitsemaan muutokset.

Voit päivittää ostotilauksen valitsemalla vastauksessa **Käsittele ostotilauksen päivitys** tai voit tehdä päivityksen yksi rivi kerrallaan. Otsikossa ja riveillä oleva **Onko ostotilauksen päivitys käsitelty?** -kenttä ilmaisee, onko järjestelmä käsitellyt otsikon tai rivit ostotilauksen siten, että ostotilaus on päivitetty vastauksesta tulevilla muutoksilla. Voit suorittaa **Käsittele ostotilauksen päivitys** -toiminnon vain kerran samassa otsikossa tai samalla rivillä.

Kaikkia ehdotettuja muutoksia ei voida päivittää ostotilaukseen. Vain ostotilauksen otsikon ja päivämäärien päivitykset ja rivien määrät voidaan päivittää automaattisesti. Muut muutokset täytyy päivittää manuaalisesti ostotilaukseen. Tässä tapauksessa **Onko ostotilauksen päivitys käsitelty?** -kentän arvo on **Manuaalinen päivitys**. Jos toimittaja esimerkiksi ehdottaa rivin jakamista aikatauluksi, muutos on tehtävä manuaalisesti.

Jos rivin tila **Hyväksytty**, sillä on oltava vahvistettu toimituspäivämäärä. Kun suoritat **Käsittele ostotilauksen päivitys** -toiminnon, tämä päivämäärä päivitetään ostotilaukseen. Huomautuksia ja liitteitä ei siirretä automaattisesti nykyiseen ostotilaukseen. Myöskään kauppasopimuksia ei arvioida ostotilauksen riveillä uudelleen, että kun päivität nykyisen ostotilauksen **Käsittele ostotilauksen päivitys** -toiminnolla.

## <a name="po-statuses-and-versions"></a>Ostotilauksen tilat ja versiot

Tässä osassa käsitellään erilaisia tiloja, joita ostotilauksella voi olla vahvistamiseen saakka. Siinä käsitellään myös ajankohtaa, jolloin ostotilauksen uudet versiot ovat toimittajan käytettävissä. Tämä vaihtelee sen mukaan, käytetäänkö ostotilauksiin muutoksenhallintaa. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versiot ja tilat, jos muutostenhallintaa ei käytetä

Alla olevassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus voi käydä läpi.

| Toiminto | Tila ja versio |
|--------|--------------------|
| Ensimmäinen ostotilauksen versio luodaan Supply Chain Managementissa. | Tilana on **Hyväksytty**. |
| Ostotilaus lähetetään toimittajalle. | Versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**. |
| Toimittaja lähettää **Hyväksytään muutosten kera** -vastauksen. | Tilana on edelleen **Ulkoisessa tarkistuksessa**. |
| Teet joitakin toimittajan pyytämiä muutoksia. | Tilaksi muuttuu **Hyväksytty**. |
| Lähetät ostotilauksen uuden version toimittajalle. | Uusi versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**. |
| Toimittaja hyväksyy ostotilauksen uuden version. | Tila on edelleen **Ulkoisessa tarkistuksessa**, ellei toimittajatiliä ei ole määritetty siirtämään ostotilauksia automaattisesti **Vahvistettu**-tilaan, kun toimittaja hyväksyy ne. |

Toimittajien ei tarvitse vahvistaa ostotilausta toimittajayhteistyöliittymässä. He voivat lähettää myös sähköpostiviestin tai ilmoittaa ostotilauksen hyväksymisestä muiden kanavien kautta. Voit sitten vahvistaa tilauksen manuaalisesti. Saat siinä tapauksessa varoituksen, joka ilmoittaa, että tilauta vahvistetaan, vaikka toimittaja ei ole vastannut siihen. Ostotilaus näkyy tämän jälkeen vahvistushistoriassa avoimena vahvistettuna tilauksena, johon ei ole vastattu. Toimittaja ei voi enää vahvistaa tai hylätä ostotilausta.

> [!NOTE]
> Muissa Supply Chain Managementin prosesseissa käytettävissä oleva ostotilauksen versio on aina uusin versio, vaikka kyseistä versiota ei olisi vielä rekisteröity toimittajayhteistyöliittymässä.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versiot ja tilat, jos muutostenhallintaa käytetään

Jos ostotilauksen muutoksenhallinta on otettu käyttöön, ostotilaukset siirtyvät **Hyväksytty**-tilaan hyväksyntätyönkulun mukaisesti. Tätä prosessia ei näy toimittajalle.

Seuraavassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus saattaa käydä läpi muutostenhallinnan ollessa käytössä. Versio rekisteröidään ostotilauksen hyväksymisen yhteydessä eikä silloin, kun ostotilaus lähetetään toimittajalle tai vahvistetaan.

| Toimenpide | Tila ja versio |
|--------|--------------------|
| Ensimmäinen ostotilauksen versio luodaan Supply Chain Managementissa. | Tilana on **Luonnos**. |
| Ostotilaus lähetetään hyväksyntäprosessiin. (Hyväksyntäprosessi on sisäinen prosessi, johon toimittaja ei osallistu.) | Tila vaihtuu **Luonnos**-tilasta **Tarkistuksessa**-tilan kautta **Hyväksyminen**-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Hyväksytty ostotilaus rekisteröidään versiona. | 
| Ostotilaus lähetetään toimittajalle. | Versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**. |
| Ostotilaus päivitetään tekemällä joitakin toimittajan pyytämiä muutoksia vastauksessa manuaalisesti tai **Käsittele ostotilauksen päivitys** -toiminnolla. | Tilaksi palautuu **Luonnos**. |
| Ostotilaus lähetetään uudelleen hyväksyntäprosessiin. | Tila vaihtuu **Luonnos**-tilasta **Tarkistuksessa**-tilan kautta **Hyväksyminen**-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Järjestelmä voidaan vaihtoehtoisesti määrittää siten, että tiettyihin kenttiin tehdyt muutokset eivät vaadi uudelleenhyväksyntää. Tässä tapauksessa tilaksi vaihtuu ensin **Luonnos**, minkä jälkeen se päivittyy automaattisesti **Hyväksytty**-tilaksi. Hyväksytty ostotilaus rekisteröidään uutena versiona. |
| Lähetät ostotilauksen uuden version toimittajalle. | Uusi versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**. |
| Toimittaja hyväksyy ostotilauksen uuden version. | Tilaksi vaihtuu **Vahvistettu** joko automaattisesti tai kun saat vastauksen toimittajalta ja vahvistat sitten ostotilauksen. |

## <a name="sharing-information-about-consignment-inventory"></a>Tavaralähetysvaraston tietojen jakaminen

Jos käytät tavaralähetysvarastoa, toimittajat voivat tarkastella seuraavien sivujen tietoja toimittajayhteistyöliittymässä:

- **Tavaralähetysvarastoa pienentävät ostotilaukset** – Tavaralähetysvaraston ostotilaukset luodaan, kun varaston omistajuus vaihtuu toimittajalta yrityksellesi. Tuotteen vastaanotto kirjataan samaan aikaan. Nämä tavaralähetyksen ostotilaukset näytetään vain **Tavaralähetysvarastoa vähentävät ostotilaukset** -sivulla. Niitä ei ole **Toimittajayhteistyö**-moduulin **Kaikki vahvistetut ostotilaukset** -sivulla.
- **Tavaralähetysvarastosta vastaanotetut tuotteet** – Tällä sivulla on luettelo kaikista tapahtumista, joissa tuotteiden omistajuus on siirretty toimittajalta yrityksellesi. Näiden tietojen avulla toimittajat voivat laskuttaa asiakasta.
- **Käytettävissä oleva tavaralähetysvarasto** – Tällä sivulla näytetään toimittajan omistama käytettävissä oleva tavaralähetysvarasto, joka on vastaanotettu varastoosi.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Tarjouspyyntöjen käsitteleminen toimittajayhteistyötä käytettäessä

Tässä osassa käsitellään asiakkaiden ja toimittajien välistä viestintää tarjouspyyntöprosessin aikana. Siinä selitetään myös, miten tiedot välitetään toimittajille. Yleiskatsaus tarjousprosessin tuesta on kohdassa [Tarjouspyyntöjen yleiskatsaus](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Vaihtoehdot, liitteet, muutokset ja palautukset

- **Vaihtoehdot** – Voit määrittää tarjouspyyntötapauksen otsikossa, että vaihtoehdot ovat sallittuja luettelon ulkopuolisille nimikeriveille. Kun vaihtoehdot on otettu käyttöön, toimittajat voivat lisätä kullekin pyydetylle riville vaihtoehtoisen rivin.
- **Liitteet** – Liitteitä voi lisätä sekä tarjouspyyntötapauksen otsikko- että rivitasolla. Liitteet voidaan luokitella sisäisiksi tai ulkoisiksi. Vain asiakas voi tarkastella sisäisiä liitteitä, kun taas ulkoiset liitteet ovat toimittajien nähtävissä lähettämisen jälkeen.

    Toimittajat voivat myös lisätä liitteitä vastatessaan tarjoukseen. Asiakkaat voivat tarkastella näitä liitteitä sen jälkeen, kun toimittaja on lähettänyt vastauksen tarjoukseen. Toimittajien lisäämät liitteet luokitellaan aina ulkoisiksi liitteiksi. Voit arvioida toimittajan tarjouksen yhteydessä lähettämän liitteen valitsemalla **Tarjouksen liitteet** tai **Tarjousrivin liitteet**.
    
    Voit avata tarjouspyyntötapauksen mukana lähetetyt liitteet napsauttamalla vastauksessa olevaa asiakirjan käsittelyn paperiliitinsymbolia.

- **Muutokset** – Kun muutos on valmis, aiemmin luodut tarjouksen vastaukset poistetaan, jotta ne voidaan korvat päivitetyillä arvoilla. Tietoja, kuten edellisten tarjouksen vastausten rivihintaa ja määrää, voidaan tarkastella tarjouspyyntötapauksen kirjauskansioiden avulla.

    Voit pakottaa muutosten käsittelemisen valitsemalla **Hankintaparametrit**-sivun **Tarjouspyynnöt**-pikavälilehden **Lukitse tarjouspyynnöt, kun ne on lähetetty** -asetukseksi **Kyllä**. (Tämän vaihtoehto on määritetty ja pakollinen julkisella sektorilla.)

- **Palautukset** – Jos toimittaja on lähettänyt tarjouksen mutta tarjouspyyntötapaus edellyttää lisätietoja tai tietojen muokkausta, asiakas voi palauttaa tarjouksen toimittajalle. Aiemmin lähetetyn tarjouksen tiedot säilytetään ja toimittaja voi tehdä pyydetyt muutokset ilman, että tarjousprosessi olisi aloitettava alusta.

## <a name="public-sector-extensions"></a>Julkisen sektorin laajennukset

Julkisen sektorin laajennetut toiminnot sallivat tarjouspyyntötapauksen lähettämisen toimittajille ja sen julkaisemisen. Kun tarjouspyyntö julkaistaan, kuka tahansa tietoja pyytävä voi tarkastella työtä, joka vastaa useimpia julkisen sektorin säädöksiä. Kaikki käytettävissä olevat työt näkyvät **Avaa julkaistut tarjouspyynnöt** -luettelosivulla. Peruutettuja, odottavia tai valittuja tarjouspyyntöjä voi tarkastella **Suljetut julkaistut tarjouspyynnöt** -luettelosivulla. Näitä asiakirjoja voi tarkastella myös Supply Chain Managementin ulkopuolisessa sivustossa seuraavien tietoyksiköiden integraation ansiosta:

- Julkaistut tarjouspyynnöt
- Julkaistut tarjouspyyntöjen rivit
- Julkaistujen tarjouspyyntöjen otsikoiden liitteet

Näiden yksiköiden kautta avoimet ja suljetut työt ovat sellaisten henkilöiden nähtävissä, jotka eivät ole Supply Chain Managementin käyttäjiä, mutta joilla on ulkoisen sivuston anonyymi käyttöoikeus. Tarjouspyyntöprosessin parametrit määrittävä käyttäjä voi lisäksi määrittää sähköpostimallin laajennetulla **Lähetä ja julkaise** -toiminnolla. Kun hankinta-asiantuntija luo sitten tarjouspyyntötapauksen, hänen on valittava sähköpostimalli, joka lähettää tarvittavat tiedot tarjouspyyntötapauksen toimittajille. 

Tarjouspyyntöprosessin parametrit määrittävä käyttäjä voi luoda useita sähköpostimalleja. Näissä sähköpostimalleissa voi olla sekä staattista tekstiä että seuraavat korvattavat tunnisteet. Tunnisteet korvataan tilannekohtaisilla arvoilla sähköpostia luotaessa.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Jos muutos on välttämätön ja se lähetetään tarjouspyynnön lähettämisen jälkeen, tarjouspyyntö lähetetään uudelleen kaikille kutsutuille toimittajille. Myös julkaistu asiakirja päivitetään **Avaa julkaistut tarjouspyynnöt** -sivulla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
