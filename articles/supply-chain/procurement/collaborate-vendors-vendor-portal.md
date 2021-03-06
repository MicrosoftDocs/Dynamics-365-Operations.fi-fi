---
title: Yhteistyö toimittajien kanssa Toimittajaportaalissa
description: Tässä aiheessa kuvataan, miten ostoedustajat voivat tehdä Toimittajaportaalissa yhteistyötä ulkoisten toimittajien kanssa ostotilauksen vahvistusprosessin aikana. Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja 2016 toukokuun versioita.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2fa295c71fb82b4168123970fee6ba71d293e3c8
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189665"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Yhteistyö toimittajien kanssa toimittajaportaalissa

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten ostoedustajat voivat tehdä Toimittajaportaalissa yhteistyötä ulkoisten toimittajien kanssa ostotilauksen vahvistusprosessin aikana. Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja toukokuun 2016 versioita.

Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja 2016 toukokuun versioita. Lisätietoja siitä uudesta toimittajayhteistyötoiminnosta on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md).  

Toimittajaportaali on tarkoitettu toimittajille, joilla ei ole sähköisten tietojen vaihdon (EDI) Microsoft Dynamics AX -integrointia ostotilausten tietojen vaihtoa varten. Portaalissa ostoedustajat voivat lähettää ostotilauksen toimittajalle ja vastaanottaa Vahvistettu- tai Hylätty-vastauksen suoraan Dynamics AX:ään.  

Prosessi voidaan määrittää siten, että toimittajan vahvistus vahvistaa tilauksen automaattisesti. Tällöin seurantaa tarvitaan vain harvoin, eli kun tilaus hylätään tai jos toimittajan vahvistus kirjataan vastauksena, mutta ostotilauksen tilaksi ei päivity **Vahvistettu** vahvistusprosessissa ilmenneen ongelman takia.

## <a name="po-confirmation-and-rejection"></a>Ostotilauksen vahvistus ja hylkääminen
Ostotilaukset laaditaan Dynamics AX:ssä. Kun sinulla on ostotilaus, jonka tila on **Hyväksytty**, voit lähettää sen toimittajalle luomalla vahvistuspyynnön. Jos haluat kiinnittää toimittajan huomion uuteen ostotilaukseen, voit myös lähettää ostotilauksen sähköpostitse käyttämällä tulostuksenhallintajärjestelmää. Ostotilaus näkyy Toimittajaportaalissa, ja siihen sisältyy vaihtoehto, jota käyttämällä toimittaja voi vahvistaa tai hylätä sen. Toimittaja voi myös lisätä esimerkiksi ostotilaukseen tehtäviä muutoksia koskevia kommentteja.  

Toimittajaportaalissa toimittaja voi tarkastella tilausrivejä. Nämä rivit sisältävät tietoja, kuten ulkoisen tuotenumeron, dimensioita, hintatietoja, määrän, toimituspäivä sekä toimitusosoitteen. Toimittaja voi luoda raportin, jossa näkyvät ostotilauksen tiedot ja kokonaishinta. Toimittaja saa itseään koskevat kulut näkyviin napsauttamalla otsikon tai tilausrivien **Kulut**-painiketta. Toimittajat voivat tuoda ostotilaustiedot omiin järjestelmiinsä käyttämällä **Vie Exceliin** -toimintoa.  

Alla olevassa taulukossa näkyy tyypillinen tietojen vaihto riippuen siitä, miten toimittaja vastaa, kun lähetät hänelle ostotilauksen vahvistusta varten.

| Vastaustyyppi                                                                                                  | Tulos                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toimittaja vahvistaa tilauksen. Järjestelmä määritetään vahvistamaan ostotilaus automaattisesti, kun toimittaja vahvistaa sen.    | Tilauksen tilaksi päivitetään **Vahvistettu** . Jos jokin estää tilauksen päivittämisen, toimittajan vastaukseksi tallennetaan silti **Vahvistettu**, mutta ostotilauksen tilana pysyy **Ulkoisessa tarkistuksessa**.                                                                       |
| Toimittaja vahvistaa tilauksen. Järjestelmää ei määritetä vahvistamaan ostotilaus automaattisesti, kun toimittaja vahvistaa sen. | Toimittajan vastaukseksi tallennetaan **Vahvistettu**, mutta ostotilaus jää **Ulkoisessa tarkistuksessa** -tilaan.                                                                                                                                                                                      |
| Toimittaja hylkää tilauksen.                                                                                     | Toimittajan vastaukseksi tallennetaan **Hylätty**, ja ostotilaus jää **Ulkoisessa tarkistuksessa** -tilaan. Hylkäys vastaanotetaan yhdessä syyn ja muutosehdotuksen, kuten vaihtoehtoisen toimituspäivän, kanssa. Päivitä ostotilaus ja lähetä sitten uusi versio vahvistettavaksi. |

## <a name="changes-to-a-po"></a>Ostotilauksen muutokset
Kun sinun tarvitsee muuttaa jo vahvistettua ostotilausta, voit lähettää toimittajalle uuden ostotilauksen Toimittajaportaalin kautta. Uuden ostotilauksen version loppuliite osoittaa, että kyseessä on aiemmin lähetetyn ostotilauksen muokattu versio. Toimittajaportaalissa toimittajat voivat seurata tilaushistoriaa. Ostotilauksen aiemmin vahvistettu versio pysyy vahvistettujen tilausten luettelossa, kunnes uusi ostotilaus on vahvistettu.  

Kun peruutat ostotilauksen, tilaksi palautuu **Hyväksytty**. Sinun on lähetettävä ostotilaus takaisin toimittajalle Toimittajaportaalin kautta, jotta toimittaja voi vahvistaa tai hylätä peruutuksen. Peruutuksen vahvistuksen jälkeen ostotilaus näkyy toimittajan vahvistettujen ostotilausten luettelossa **Peruutettu**-tilassa.

## <a name="versions-status-transitions-and-change-management"></a>Versiot, tilanmuutokset ja muutostenhallinta
Kun ostotilaus lähetettään toimittajalle, se rekisteröidään järjestelmään tiettynä ostotilauksen versiona ja se siirtyy **Hyväksytty**-tilasta **Ulkoisessa tarkistuksessa** -tilaan. Jos ostotilausta muutetaan myöhemmin, siitä luodaan uusi versio ja tilaksi palautuu **Hyväksytty** (tai **Luonnos**, jos muutostenhallinta on käytössä).  

Alla olevassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus voi käydä läpi.

| Toiminto                                                   | Tila ja versio                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Ensimmäinen ostotilauksen versio luodaan Dynamics AX:ssä. | Tilana on **Hyväksytty**.                                                                           |
| Ostotilaus lähetetään Toimittajaportaaliin                     | Versio rekisteröidään Toimittajaportaaliin, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**.    |
| Teet joitakin toimittajan pyytämiä muutoksia.  | Tilaksi palautuu **Hyväksytty**.                                                            |
| Lähetät ostotilauksen uuden version Toimittajaportaaliin. | Uusi versio rekisteröidään Toimittajaportaaliin, ja tilaksi vaihtuu **Ulkoisessa tarkistuksessa**. |
| Toimittaja hyväksyy ostotilauksen uuden version.           | Tilaksi vaihtuu **Vahvistettu**.                                                                |

Jos haluat nähdä toimittajalle lähetetyt ostotilauksen versiot ja toimittajan vastaukset, valitse ostotilauksessa **Kirjauskansiot** &gt; **Vahvistuspyynnöt**.  

Toimittajalle vastausta varten lähetetyt tilaukset, joiden tilana on **Ulkoisessa tarkistuksessa**, näytetään joko **Toimittajaportaaliin lähetetyt ostotilaukset – odottaa vastausta**- tai **Toimittajaportaaliin lähetetyt ostotilaukset – vastaus edellyttää toimia** -luettelossa. Kun muutat toimittajalle lähetettyä tilausta niin, että tilaksi palautuu **Hyväksytty**, se ei enää näy näissä luetteloissa. Jos haluat tarkistaa, onko toimittajalta saatu aiemmin vastausta tilaukseen, valitse **Kirjauskansiot** &gt; **Vahvistuspyynnöt**.  

Toimittajien ei tarvitse vahvistaa ostotilausta Toimittajaportaalissa. He voivat lähettää myös sähköpostiviestin tai ilmoittaa ostotilauksen hyväksymisestä muissa kanavissa. Tämän jälkeen voit vahvistaa tilauksen manuaalisesti Dynamics AX:ssä. Tällöin saat varoituksen, kun tilaus on vahvistettu, vaikka toimittajalta ei olisi saatu vastausta. Ostotilaus näkyy tämän jälkeen Toimittajaportaalissa vahvistushistoriassa avoimena vahvistettuna tilauksena, johon ei ole vastattu. Lisäksi toimittaja ei pysty enää vahvistamaan tai hylkäämään ostotilausta.  

**Huomautus:** Ostotilauksen versio, joka on käytettävissä muissa Dynamics AX -prosesseissa, on aina uusin versio, vaikka kyseistä versiota ei olisi vielä rekisteröity.

### <a name="change-management"></a>Muutostenhallinta

Jos olet ottanut muutoksenhallinnan käyttöön ostotilaukselle, ostotilaus käy läpi hyväksymistyökulun, jotta se voidaan lopulta siirtää **Hyväksytty**-tilaan. Tätä prosessia ei näy toimittajalle.  

Kun ostotilaukselle on otettu muutoksenhallinta käyttöön, versio rekisteröidään ostotilauksen hyväksymisen yhteydessä, ei silloin, kun ostotilaus lähetetään toimittajalle tai vahvistetaan.  

Seuraavassa taulukossa on esimerkki tila- ja versiomuutoksista, jotka ostotilaus saattaa käydä läpi muutostenhallinnan ollessa käytössä.


|                                                    Toiminto                                                     |                                                                                                                                                                                                                      Tila ja versio                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           Ensimmäinen ostotilauksen versio luodaan Dynamics AX:ssä.                            |                                                                                                                                                                                                            Tilana on <strong>Luonnos</strong>.                                                                                                                                                                                                             |
| Ostotilaus lähetetään hyväksyntäprosessiin. (Tämä on sisäinen prosessi, johon toimittaja ei osallistu.) |                                                                                                                        Tila vaihtuu <strong>Luonnos</strong>-tilasta <strong>Tarkistuksessa</strong>-tilan kautta <strong>Hyväksyminen</strong>-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Hyväksytty ostotilaus rekisteröidään versiona.                                                                                                                        |
|                                      Ostotilaus lähetetään toimittajaportaaliin                                      |                                                                                                                                                                      Versio rekisteröidään Toimittajaportaaliin, ja tilaksi vaihtuu <strong>Ulkoisessa tarkistuksessa</strong>.                                                                                                                                                                       |
|                            Teet joitakin toimittajan pyytämiä muutoksia.                            |                                                                                                                                                                                                    Tilaksi palautuu <strong>Luonnos</strong>.                                                                                                                                                                                                     |
|                              Ostotilaus lähetetään uudelleen hyväksyntäprosessiin.                               | Tila vaihtuu <strong>Luonnos</strong>-tilasta <strong>Tarkistuksessa</strong>-tilan kautta <strong>Hyväksyminen</strong>-tilaan, jos ostotilausta ei hylätä hyväksymisprosessin aikana. Järjestelmä voidaan vaihtoehtoisesti määrittää siten, että tiettyihin kenttiin tehdyt muutokset eivät vaadi uudelleenhyväksyntää. Tässä tapauksessa tilaksi vaihtuu ensin <strong>Luonnos</strong>, minkä jälkeen se päivittyy automaattisesti <strong>Hyväksytty</strong>-tilaksi. Hyväksytty ostotilaus rekisteröidään uutena versiona. |
|                           Lähetät ostotilauksen uuden version Toimittajaportaaliin.                            |                                                                                                                                                                    Uusi versio rekisteröidään Toimittajaportaaliin, ja tilaksi vaihtuu <strong>Ulkoisessa tarkistuksessa</strong>.                                                                                                                                                                     |
|                                Toimittaja hyväksyy ostotilauksen uuden version.                                 |                                                                                                                                                     Tilaksi vaihtuu <strong>Vahvistettu</strong> joko automaattisesti tai kun saat vastauksen toimittajalta ja vahvistat sitten ostotilauksen.                                                                                                                                                     |

## <a name="additional-resources"></a>Lisäresurssit

[Toimittajaportaalin käyttäjäsuojaus](configure-security-vendor-portal-users.md)

[Toimittajayhteistyön laskutustyötila](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]