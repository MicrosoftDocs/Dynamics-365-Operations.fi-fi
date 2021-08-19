---
title: Ostohyvitysten hallintamoduulin yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Supply Chain Managementin ostohyvitysten hallintamoduulin yleiskatsaus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 136e528093e6e73ffe090cea0c02a4cdbf787c5efc3d9c0664869c995a682daa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720249"
---
# <a name="rebate-management-module-overview"></a>Ostohyvitysten hallintamoduulin yleiskatsaus

[!include [banner](../includes/banner.md)]

**Ostohyvitysten hallinta** -moduulin avulla voit luoda sopimuksia yrityksen ja sen asiakkaiden tai toimittajien välille ja näin laskea ostohyvitykset, vähennykset ja maksuhyvitykset. Ostohyvitysten hallinta seuraa ja ylläpitää ostohyvitys- ja vähennystapahtumia keskitetyssä sijainnissa, jossa käyttäjät voivat tehokkaasti luoda, tarkistaa ja käsitellä niitä.

Ostohyvitysten hallinta tukee *ostohyvitysten* luontia, ylläpitoa ja käsittelyä. Ostohyvitys on myyjän tai ostajan palautus ostohinnasta. Ostohyvitykset perustuvat yleensä tavaroiden tietyn määrän tai arvon ostoon tiettynä ajanjaksona. Toisin kuin alennukset, ostohyvitykset tehdään, kun ostosumma on kokonaan laskutettu.

Ostohyvitysten hallinta tukee myös *vähennyksiä*. Vähennys on kompensaatio, korvaus tai maksu, joka maksetaan joko lisenssistä tai immateriaaliomaisuuden, kuten tekijänoikeuden tai patentin, käyttöoikeudesta tai oikeudesta käyttää luonnonresurssia esimerkiksi kalastukseen, metsästykseen tai kaivostoimintaan. Vähennykset lasketaan yleensä prosenttiosuutena toteutuneen käytön tuotoista tai voitosta. Mitä enemmän immateriaaliomaisuutta tai luonnonresurssia käytetään, sitä suurempi on vähennys, joka toteutuu.

Ostohyvitysten hallinta tukee myös asiakkaiden *rojalteja*. Rojaltit ovat maksuja, jotka yksi osapuoli maksaa lisenssinhaltijalle resurssin käyttöoikeudesta.

Ostohyvitysten hallinnan avulla voit määrittää varausten, ostohyvitysten ja poiskirjausten kirjausprofiilit. Kirjaukset voidaan myös määrittää tietylle asiakkaalle tai toimittajalle. Näin sopimuksia, jotka eivät koske kaikkia asiakas- tai toimittajaskenaarioita, voidaan seurata kirjauksien avulla.

Ostohyvitystapahtumat luodaan automaattisesti erätöissä valitun ja ajoitetun laskentamenetelmän perusteella. Lisäksi voit määrittää työnkulut sopimusten hallintaa, tarkistusta ja hyväksyntää varten.

## <a name="basis-calculation"></a>Perusteen laskenta

Asiakkaan ostohyvitykset, asiakkaan rojaltit ja toimittajan ostohyvitykset voivat kaikki käyttää liiketoimintatarpeiden mukaan eri perusteita:

- Asiakkaan ostohyvitykset voivat perustua myyntitilauksiin, toimitusilmoituksiin tai laskuihin.
- Asiakkaan rojaltit voivat perustua myyntitilauksiin, toimitusilmoituksiin tai maksettuihin laskuihin.
- Toimittajan ostohyvitykset voivat perustua joko ostotilauksiin tai myyntitilauksiin. Ne voidaan laskea ostohyvityksen toimittajalta ostettujen ja asiakkaille myyntilaskujen kautta myytyjen tuotteiden perusteella.

## <a name="flexible-calculations"></a>Joustavat laskelmat

Ostohyvityksen laskentakaudet ovat käytettävissä sekä asiakas- että toimittajasopimuksille. Laskentakausi määrittää sopimuksen pituuden, laskentavälin ja laskentakauden. Ostohyvitykset voidaan jaksottaa ostohyvityskauden aikana hyväksyttyjen tuotteiden myyntitilausmäärien tai -summien perusteella.

Kullekin sopimuslaskelmalle voidaan määrittää jokin seuraavista kausista:

- Lasku
- Päivä
- Viikko
- Kuukausi
- Vuosineljännes
- Vuosi(a)
- Mukautettu kausi
- Aiemmin lueteltujen kausien mikä tahansa kerrannainen

Laskelmaa voidaan soveltaa yksittäisiin asiakkaisiin ja tuotteisiin, asiakas- ja tuoteryhmiin tai kaikkiin asiakkaisiin ja tuotteisiin. Ostohyvityksillä, joissa on useita erittelyrivejä, voi olla eri päivämäärävälit. Varaus- ja vaatimuskaudet voivat vaihdella. Varaukset voidaan esimerkiksi käsitellä joka päivä, kun taas vaatimukset käsitellään kerran kuukaudessa.

Ostohyvitykset voidaan konfiguroida monien erilaisten parametrien perusteella. Ne voidaan konfiguroida esimerkiksi prosenttiosuutena, hintana tai kiinteänä summana. Päälaskentatapoja on neljä:

- Vaiheittainen
- Kumulatiivinen
- Juokseva
- Kokonaisarvo

Myös muut ostohyvitykset voivat vähentää ostohyvityksen laskentatuloksia sen mukaan, onko ostohyvitys määritetty laskemaan nettosumman perusteella.

Toimittajapuolella myyntitilauksiin perustuvat ostohyvitykset voivat laskea hinnan FIFO-säännön, viimeisimmän ostohinnan, keskimääräisen ostohinnan tai myyntihinnan perusteella.

## <a name="rebate-target-transactions"></a>Ostohyvityksen kohdetapahtumat

Ostohyvityssopimuksen tuottamat tulokset voivat olla taloudellisia tuloksia tai nimikkeitä.

Taloudelliset tulokset määräytyvät sopimukseen kirjausprofiilista liitetyn maksutyypin mukaan. Nämä tulokset voivat sisältää asiakkaan vähennyskirjauskansioita, vapaatekstilaskuja ja toimittajan laskuja. Valvontatarkoituksia varten taloudellisen ostohyvityksen kohdetapahtumisissa on viite alkuperäiseen ostohyvityssopimukseen.

Nimiketulokset luovat maksuttoman nimikkeiden myyntitilauksen asiakkaan ostohyvitykselle ja ostotilauksen toimittajan ostohyvitykselle. Nimikkeen ostohyvityksen kohdetapahtumien vaihtoehtojen avulla määritetään, mikä ostohyvitysviite on syötettävä maksuttomien nimikkeiden myyntitilaukseen tai ostotilaukseen.

## <a name="accurate-rebate-calculations"></a>Tarkat ostohyvityslaskelmat

Liitettyjen sopimusten yhdistelmä, laskelmien tiheys, laskentaperuste ja valittu laskentamenetelmä määrittävät ostohyvityslaskelmien tarkkuuden. Ostohyvitysvarauksia voidaan käyttää kirjattujen ja vaadittujen arvojen jaksottamiseen.

Varauksia voidaan hallita päivittäin, viikoittain, kuukausittain tai mukautetun kauden mukaan. Toiminto voi kuitenkin kohdistaa tai maksaa ostohyvityksen tai vastaanottaa sen maksun määritetyllä tiheydellä, joka on sama tai pidempi kuin varausväli. Alennuksia käytetään samalla tiheydellä kuin ostohyvitystä. Käyttäjät voivat helposti muuttaa tilaus- tai maksusummia milloin tahansa maksun aikana.

Käyttäjien ei enää tarvitse käsitellä sopimuksia tai varauksia kahdessa vaiheessa. Varaukset ja poiskirjaukset kirjataan suoraan kirjanpitoon. Lisäksi hyvityslaskut voidaan luoda automaattisesti. Tämän vuoksi ostoreskontraan ja myyntireskontraan on täysi integrointi. Käsittelyn aikana laskelmissa voidaan käsitellään tilitysalennuksia, maksettuja laskuja, kauppa-alennuksia ja olemassa olevia hyvityslaskuja sen varmistamiseksi, että summat ja arvot lasketaan oikein.

Kun ostohyvitykset lasketaan, prosessi luo tapahtumat, joita voidaan tarkastella ennen kirjauksen tekemistä. Erillinen prosessi kirjaa ostohyvityksen hallintatapahtumat. Tämän jälkeen ehdotettuihin tapahtumiin kirjauksen aikana voidaan luoda kirjauskansio, hyvityslasku- tai veloitustapahtuma. Raportointi-ilmoitukset ja tapahtumaluettelot ovat saatavissa vaatimustenmukaisuuden, tehokkuuden ja läpinäkyvyyden varmistamiseksi.

## <a name="guaranteed-royalty-payments"></a>Taatut rojaltimaksut

Ostohyvitysten hallinnassa automaattinen maksujen luonti mahdollistaa rojaltien nopean ja helpon hallinnan, vaikka käytettäisiin taattuja vähimmäissummia.

## <a name="maximizing-spend-versus-rebates"></a>Kulujen maksimointi ja ostohyvitykset

Toimittajat ja tuotteet voidaan ryhmitellä alueen mukaan, ja erilaisia tarjouksia voidaan tarjota tapahtuman maasta tai alueesta riippuen. Kun käyttäjät valitsevat tuotteita, he voivat määrittää sisällytetyt nimikkeet ja ostohyvityksen tilitykseen käytettävien nimikkeiden määrän.
