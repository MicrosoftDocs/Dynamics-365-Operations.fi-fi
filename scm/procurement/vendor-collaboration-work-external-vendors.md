---
title: "Toimittajayhteistyö ulkoisten toimittajien kanssa"
description: "Tässä aiheessa kuvataan, miten ostoedustajat voivat tehdä yhteistyötä ulkoisten toimittajien kanssa ja vaihtaa ostotilauksia ja tavaralähetysvarastoa koskevia tietoja."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c8947f9335b3a2de83ab00bad1043ee14d35f2c8
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Toimittajayhteistyö ulkoisten toimittajien kanssa

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten ostoedustajat voivat tehdä yhteistyötä ulkoisten toimittajien kanssa ja vaihtaa ostotilauksia ja tavaralähetysvarastoa koskevia tietoja.

**Toimittajayhteistyö**-moduuli on tarkoitettu toimittajille, joilla ei ole sähköisten tietojen vaihdon (EDI) Microsoft Dynamics 365 for Operations -integrointia. Sen avulla toimittajat voivat käsitellä ostotilauksia, laskuja ja luovutetun varaston tietoja. Tässä aiheessa kuvataan, miten voit tehdä yhteistyötä ulkoisten toimittajien kanssa, jotka käyttävät toimittajayhteistyöliittymää työskentelyyn myyntipisteissä ja tavaralähetysvarastoja. Siinä myös kuvataan miten tietty toimittaja voi käyttää toimittajayhteistyötä ja miten määritetään tiedot, jotka näkyvät kaikille toimittajille, kun he vastaavat ostotilaukseen. Lisätietoja siitä, mitä ulkoiset toimittajat voivat tehdä toimittajan toimittajayhteistyöliittymällä, on kohdassa [Toimittajayhteistyö asiakkaiden kanssa](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Lisätietoja siitä, kuinka toimittajat voivat käyttää toimittajayhteistyötä laskutusprosesseissa, on kohdassa [Toimittajayhteistyön laskutustyötila](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Tietoja siitä, miten uusia toimittajayhteistyön käyttäjiä voidaan valmistella, on kohdassa [Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Ostotilaukseen vastaaville toimittajille näytettävien tietojen hallinta
Kun toimittajat vastaavat lähettämääsi ostotilaukseen, he näkevät valintaikkunan, jossa ostotilaus pitää hyväksyä, hylätä tai hyväksyä muutosten kera. Tässä vaiheessa toimittajalle näytettävät tiedot voivat olla yrityskohtaisia, joten voit määrittää tekstin, jotka näkyvät jokaisessa kolmessa vahvistussanomassa. Teksti voi esimerkiksi ilmoittaa toimittajalle tietoja prosessin seuraavista vaiheista tai noudatettavista ehdoista.  

Määritä teksti, joka näkyy ostotilauksen vastauksessa:

1.  Avaa **Ostotilauksiin vastaaville toimittajille tarkoitetut tiedot** -sivu.
2.  Valitse yksi seuraavista vastaustyypeistä:
3.  Valitse **Muokkaa**.
4.  Syötä tiedot, jotka haluat näyttää toimittajille, ruudussa **Tietosanoma**.

Jos haluat lisätä sanomat useammalla kuin yhdellä kielellä, luo eri viestit tarvittavilla kielikoodeilla. Viesti näytetään toimittajalle tämän käyttökielellä.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Toimittajayhteistyön asetusten määrittäminen tiettyä toimittajaa varten
Järjestelmänvalvojan määrittää toimittajayhteistyön yleiset asetukset Dynamics 365 for Operationsiin. Esimerkiksi he määrittävät, mitkä suojausroolit ovat käytettävissä kaikille toimittajille, joiden kanssa tehdään yhteistyötä. On myös joitakin asetuksia, jotka voivat olla erilaiset jokaiselle toimittajatilille ja jotka pitää määrittää:

-   Toimittajayhteistyön käyttöönotto.
-   Päätä, näkeekö toimittaja hintatietoja.

### <a name="enable-vendor-collaboration"></a>Toimittajayhteistyön käyttöönotto

Ennen kuin käyttäjätilit voidaan luoda ulkoiselle toimittajalle, on määritettävä toimittajatili, jota he voivat käyttää toimittajayhteistyössä. Voit tehdä tämän määrittämällä **Yhteistyön aktivointi** kentän arvoksi aktiivinen **Yleistä**-välilehdessä **Toimittajat**-sivulla. Voit valita kahdesta vaihtoehdosta:

-   **Aktiivinen (ostotilaus vahvistetaan automaattisesti)**- Ostotilaukset vahvistetaan automaattisesti, kun toimittaja hyväksyy sen ilman muutoksia.
-   **Aktiivinen (ostotilausta ei vahvisteta automaattisesti)**– Ostotilaukset on vahvistettava manuaalisesti organisaatiossasi, kun toimittaja on hyväksynyt ne.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Päätä, näkeekö toimittaja hintatietoja.

Jos haluat jakaa hintatiedot, kuten yksikköhinta, alennukset ja kulut toimittajayhteistyön liittymän kautta, sinun pitää määrittää **Ostotilauksen hinnat/summa** -asetukseksi **Kyllä** toimittajatilillä. Tämä vaihtoehto on käytettävissä **Oletusostotilaukset**-välilehdessä.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Ostotilausten käsitteleminen toimittajayhteistyötä käytettäessä
### <a name="sending-a-po-to-the-vendor"></a>Ostotilauksen lähettäminen toimittajalle

Ostotilaukset laaditaan Dynamics 365 for Operationsissa. Kun ostotilauksen tilana on **Hyväksytty**, se lähetetään toimittajalle **Lähetä vahvistettavaksi** -toiminnolla **Ostotilaus**-sivulla. Ostotilauksen tilaksi muuttuu **ulkoisessa tarkistuksessa**. Sen jälkeen, kun ostotilaus on lähetetty, toimittaja näkee sen **Tarkistettavat ostotilaukset** sivulla toimittajayhteistyöliittymässä, missä hän voi hyväksyä, hylätä tai ehdottaa muutoksia tilaukseen. Toimittaja voi myös lisätä esimerkiksi ostotilaukseen tehtäviä muutoksia koskevia kommentteja. Jos haluat kiinnittää toimittajan huomion uuteen ostotilaukseen, voit myös lähettää ostotilauksen sähköpostitse käyttämällä tulostuksenhallintajärjestelmää.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>Toimittaja hyväksyy ja vahvistaa ostotilauksen

Kun toimittaja on hyväksynyt ostotilauksen, ostotilaus vahvistetaan automaattisesti tai se täytyy vahvistaa manuaalisesti. Tähän vaikuttaa se, onko **Toimittajan aktivointi** -kentän asetus **Aktiivinen (ostotilaus vahvistetaan automaattisesti)** toimittajan puolesta tai **Aktiivinen (ostotilausta ei vahvisteta automaattisesti)**.  

Seuraavassa taulukossa näytetään tyypillinen tietojen vaihto riippuen siitä, miten toimittaja vastaa, kun lähetät heille ostotilauksen vahvistusta varten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Toimittajan vastaus</strong></td>
<td><strong>Laskutoimitus</strong></td>
</tr>
<tr class="even">
<td>Toimittaja <strong>hyväksyy</strong> tilauksen. Dynamics 365 for Operations määritetään vahvistamaan ostotilaus automaattisesti, kun toimittaja hyväksyy sen.</td>
<td>Tilauksen tilaksi päivitetään <strong>Vahvistettu</strong> . Jos jokin estää tilauksen päivittämisen, toimittajan vastaukseksi tallennetaan silti <strong>Hyväksytty</strong>, mutta ostotilauksen tilana pysyy <strong>Ulkoisessa tarkistuksessa</strong>.</td>
</tr>
<tr class="odd">
<td>Toimittaja <strong>hyväksyy</strong> tilauksen. Dynamics 365 for Operationsia ei määritetä vahvistamaan ostotilausta automaattisesti, kun toimittaja hyväksyy sen.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hyväksytty</strong>, mutta ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan.</td>
</tr>
<tr class="even">
<td>Toimittaja <strong>hylkää</strong> tilauksen.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hylätty</strong>, ja ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan. Hylkäys vastaanotetaan yhdessä toimittajan viestin kanssa.</td>
</tr>
<tr class="odd">
<td>Toimittaja <strong>hyväksyy tilauksen muutosten kera</strong>. Muutoksia on ehdotettu rivin tasolla. On mahdollista hyväksyä tai hylätä rivit. Muut mahdolliset muutokset ovat seuraavat:
<ul>
<li>Päivämäärien tai määrien muuttaminen</li>
<li>Rivien jakaminen eri toimituspäivämäärille tai määrille</li>
<li>Nimikkeen korvaaminen</li>
</ul>
Toimittaja ei voi muuttaa hintatietoja ja kuluja. Muutosehdotukset voidaan tehdä huomautuksissa.</td>
<td>Toimittajan vastaukseksi tallennetaan <strong>Hyväksytty muutosten kera</strong>, <strong></strong> mutta ostotilaus jää <strong>Ulkoisessa tarkistuksessa</strong> -tilaan.</td>
</tr>
</tbody>
</table>

**Ostotilauksen** **valmistelu** -työtilan avulla voit valvoa, mihin ostotilaukseen toimittaja on vastannut. Työtilassa on kaksi luetteloa, jotka sisältävät ostotilauksista, joiden tila on **ulkoisessa tarkistuksessa**:

-   Ulkoisessa tarkistuksessa -kohde vaatii toiminnon.
-   Ulkoisessa tarkistuksessa, odottaa toimittajan vastausta.

### <a name="changing-a-po"></a>Ostotilauksen muuttaminen

Kun sinun pitää muuttaa ostotilausta, johon on vastattu, voit lähettää toimittajalle uuden ostotilauksen version. Uuden ostotilauksen version loppuliite osoittaa, että kyseessä on aiemmin lähetetyn ostotilauksen muokattu versio. **Ostotilausten toimittajan vahvistushistoria** -sivulla sinä ja toimittaja voitte seurata jokaisen tilauksen historiatietoja. Ostotilauksen aiemmin vahvistettu versio pysyy vahvistettujen tilausten luettelossa, kunnes uusi ostotilaus on vahvistettu.

### <a name="cancelling-a-po"></a>Ostotilauksen peruuttaminen

Kun peruutat ostotilauksen, tilaksi vaihtuu **Hyväksytty**. Sinun on lähetettävä ostotilaus takaisin toimittajalle Toimittajaportaalin kautta, jotta toimittaja voi vahvistaa tai hylätä peruutuksen. Peruutuksen vahvistuksen jälkeen ostotilaus näkyy toimittajan vahvistettujen ostotilausten luettelossa **Peruutettu**-tilassa.

### <a name="adding-attachments-to-a-po"></a>Liitteiden lisääminen ostotilaukseen

Voit lisätä liitteitä, esimerkiksi tiedostoja, kuvia ja huomautuksia ostotilaukseen käyttämällä tiedostojen hallintajärjestelmää. Jos liitteeseen lisätään**Ulkoinen**-tyyppinen rajoitus, se näytetään toimittajalle kun lähetät ostotilauksen hänelle.

## <a name="purchase-order-statuses-and-versions"></a>Ostotilauksen tilat ja versiot
Tässä osassa kuvataan eri tilat, joita ostotilauksella voi olla vahvistukseen saakka, ja missä vaiheessa ostotilauksen uudet versiot ovat toimittajan käytettävissä. Erot johtuvat siitä, käytetäänkö muutostenhallintaa ostotilauksille. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Versiot ja tilat, jos muutostenhallintaa ei käytetä

Alla olevassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus voi käydä läpi.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toimenpide**                                                               | **Tila ja versio**                                                                                                                                       |
| Ensimmäinen ostotilauksen versio luodaan Dynamics 365 for Operationsissa. | Tilana on **Hyväksytty**.                                                                                                                                  |
| Ostotilaus lähetetään toimittajalle.                                            | Versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**.                                          |
| Toimittaja lähettää **Hyväksytään muutosten kera** -vastauksen.                  | Tilana on edelleen **Ulkoisessa tarkistuksessa**.                                                                                                                  |
| Teet joitakin toimittajan pyytämiä muutoksia.                  | Tilaksi muuttuu **Hyväksytty**.                                                                                                                        |
| Lähetät ostotilauksen uuden version toimittajalle.                        | Uusi versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**.                                      |
| Toimittaja hyväksyy ostotilauksen uuden version.                            | Tilana on edelleen **Ulkoisessa tarkistuksessa**, jos toimittajatiliä ei ole määritetty asettamaan ostotilausta **Vahvistettu**-tilaan, kun hän hyväksyy sen. |

Toimittajien ei tarvitse vahvistaa ostotilausta toimittajayhteistyöliittymässä. He voivat lähettää myös sähköpostiviestin tai ilmoittaa ostotilauksen hyväksymisestä muissa kanavissa. Tämän jälkeen voit vahvistaa tilauksen manuaalisesti Dynamics 365 for Operationsissa. Tällöin saat varoituksen, että tilaus on vahvistettu, vaikka toimittajalta ei olisi saatu vastausta. Ostotilaus näkyy tämän jälkeen vahvistushistoriassa avoimena vahvistettuna tilauksena, johon ei ole vastattu. Toimittaja ei pysty enää vahvistamaan tai hylkäämään ostotilausta.  

**Huomautus:** Ostotilauksen versio, joka on käytettävissä muissa 365 for Operations -prosesseissa, on aina uusin versio, vaikka kyseistä versiota ei olisi vielä rekisteröity toimittajayhteistyöliittymässä.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Versiot ja tilat, jos muutostenhallintaa käytetään

Jos muutoksenhallinta on otettu käyttöön ostotilaukselle, ostotilaus käy läpi hyväksymistyökulun, jotta se voidaan lopulta siirtää **Hyväksytty**-tilaan. Tätä prosessia ei näy toimittajalle.  

Seuraavassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus saattaa käydä läpi muutostenhallinnan ollessa käytössä. Versio rekisteröidään ostotilauksen hyväksymisen yhteydessä eikä silloin, kun ostotilaus lähetetään toimittajalle tai vahvistetaan.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toimenpide**                                                                                                    | **Tila ja versio**                                                                                                                                                                                                                                                                                                                                                                      |
| Ensimmäinen ostotilauksen versio luodaan Dynamics 365 for Operationsissa.                                      | Tilana on **Luonnos**.                                                                                                                                                                                                                                                                                                                                                                    |
| Ostotilaus lähetetään hyväksyntäprosessiin. (Tämä on sisäinen prosessi, johon toimittaja ei osallistu.) | Tila vaihtuu **Luonnos**-tilasta **Tarkistuksessa**-tilan kautta **Hyväksyminen**-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Hyväksytty ostotilaus rekisteröidään versiona.                                                                                                                                                                                                                     |
| Ostotilaus lähetetään toimittajalle                                                                                  | Versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**.                                                                                                                                                                                                                                                                       |
| Teet joitakin toimittajan pyytämiä muutoksia.                                                       | Tilaksi palautuu **Luonnos**.                                                                                                                                                                                                                                                                                                                                                    |
| Ostotilaus lähetetään uudelleen hyväksyntäprosessiin.                                                            | Tila vaihtuu **Luonnos**-tilasta **Tarkistuksessa**-tilan kautta **Hyväksyminen**-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Järjestelmä voidaan vaihtoehtoisesti määrittää siten, että tiettyihin kenttiin tehdyt muutokset eivät vaadi uudelleenhyväksyntää. Tässä tapauksessa tilaksi vaihtuu ensin **Luonnos**, minkä jälkeen se päivittyy automaattisesti **Hyväksytty**-tilaksi. Hyväksytty ostotilaus rekisteröidään uutena versiona. |
| Lähetät ostotilauksen uuden version toimittajalle.                                                             | Uusi versio rekisteröidään toimittajayhteistyöliittymään, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**.                                                                                                                                                                                                                                                                   |
| Toimittaja hyväksyy ostotilauksen uuden version.                                                                | Tilaksi vaihtuu **Vahvistettu** joko automaattisesti tai kun saat vastauksen toimittajalta ja vahvistat sitten ostotilauksen.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Tavaralähetysvaraston tietojen jakaminen
Jos käytät tavaralähetysvarastoa, toimittajat voivat käyttää toimittajayhteistyöliittymää tietojen tarkasteluun seuraavilla sivuilla:

-   **Tavaralähetysvarastoa pienentävät ostotilaukset** - Tavaralähetysvaraston ostotilaukset luodaan, kun varaston omistajuus vaihtuu toimittajalta yrityksellesi. Tuotteen vastaanotto kirjataan samaan aikaan. Nämä tavaralähetyksen ostotilaukset näytetään vain **Tavaralähetysvarastoa vähentävät ostotilaukset** -sivulla. Ne eivät sisälly **Kaikki vahvistetut ostotilaukset** -sivulle **Toimittajayhteistyö**-moduulissa.
-   **Tavaralähetysvarastosta vastaanotetut tuotteet**: Sivulla luetteloidaan kaikki tapahtumat, joissa tuotteiden omistajuus siirretään toimittajalta yrityksellesi. Näiden tietojen avulla toimittajat voivat laskuttaa asiakasta.
-   **Käytettävissä oleva tavaralähetysvarasto** - Tällä sivulla näkyy toimittajan omistama käytettävissä oleva tavaralähetysvarasto, joka on vastaanotettu varastoosi.





