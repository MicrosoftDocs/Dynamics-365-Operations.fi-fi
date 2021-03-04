---
title: Toimittajayhteistyö asiakkaiden kanssa
description: Tässä aiheessa kuvataan, miten voit käyttää ostotilauksia ja valvoa tavaralähetysvarastoa toimittajayhteistyön avulla.
author: TaylorVH
manager: tfehr
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: v-savanh
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc97b230f23056db90e654b4aea3272bb8f1ba13
ms.sourcegitcommit: 0c33864efdd66c6ac11a4f35d971c0bb4efb15db
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654337"
---
# <a name="vendor-collaboration-with-customers"></a>Toimittajayhteistyö asiakkaiden kanssa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa kuvataan, miten voit käyttää toimittajayhteistyötä työskennelläksesi asiakkaiden kanssa Microsoft Dynamics 365 Supply Chain Managementissa. Toimittajat voivat suorittaa liiketoimintaprosessien sarjan seuraavista työtiloista:

- **Ostotilauksen vahvistus** – ostotilausten seuranta ja niihin vastaaminen.
- **Toimittajan tarjoukset** – tarjouspyyntöjen tarkastelu ja niihin vastaaminen tekemällä tarjouksia.
- **Toimittajatiedot** – toimittajan päätietojen tarkastelu ja päivittäminen.
- **Laskutus** – laskujen käsittely. Tässä ohjeaiheessa ei käsitellä **Laskutus**-työtilaa. Lisätietoja kyseisestä työtilasta on kohdassa [Toimittajayhteistyön laskutustyötila](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

Toimittajat voivat seurata myös tavaralähetysvaraston tietoja.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Ostotilausten käsittely Ostotilauksen vahvistus -työtilassa

Voit vastata **Ostotilauksen vahvistus** -työtilassa ostotilauksiin, jotka on lähetetty tarkistettavaksi varten. Voit myös tarkastella asiakkaan toimintoja odottavaa ostotilausta sekä vahvistettuja mutta edelleen avoimia ostotilauksia.

**Ostotilauksen vahvistus** -työtilassa on kolme luetteloa:

- **Tarkistettavat ostotilaukset** – Luettelossa on kaikki sinulle lähetetyt ja vastausta odottavat ostotilaukset. Kun olet vastannut, ostotilaus poistuu luettelosta. Jos asiakas lähettää uuden version ostotilauksesta ennen edelliseen versioon vastaamista, vain uusin versio näkyy luettelossa.
- **Odottaa asiakkaan toimintoa** – Tässä luettelossa on kaikki ostotilauksia, joihin olet vastannut mutta joita asiakas ei ole vielä vahvistanut. Jos hyväksyt ostotilauksen, voit seurata sitä luettelossa, kunnes sen tilaksi tulee **Vahvistettu**. Jos hylkäät ostotilauksen tai hyväksyit sen muutosten kera, voit seurata sitä luettelossa, kunnes asiakas lähettää uuden version.
- **Avoimet vahvistetut ostotilaukset** – Tässä luettelossa on kaikki tililläsi olevat ostotilaukset, joiden tila on **Vahvistettu**. Kun kaikki ostotilausta vastaavat tuotteet tai palvelut on vastaanotettu, ostotilaus poistuu luettelosta.

Voit käsitellä ostotilauksia seuraavilla sivuilla:

- **Tarkistettavat ostotilaukset** – Tällä sivulla on samat tiedot kuin työtilan **Tarkistettavat ostotilaukset** -luettelossa. Luetteloa on jo käsitelty aiemmin tässä aiheessa.
- **Ostotilausten toimittajan vahvistushistoria** – Tällä sinulla on kaikki toimittajalle lähetetyt ostotilaukset ja ostotilausten kaikki versiot. Se sisältää myös kaikki toimittajan palauttamat vastaukset.
- **Avoimet vahvistetut ostotilaukset** – Tällä sivulla on samat tiedot kuin työtilan **Avoimet vahvistetut ostotilaukset** -luettelossa. Luetteloa on jo käsitelty aiemmin tässä aiheessa.
- **Kaikki vahvistetut ostotilaukset** – Tällä sivulla on kaikki vahvistetut ostotilaukset. Tämä sivulla on näkyvissä myös ne ostotilaukset, joiden tuotteet tai palvelut on vastaanotettu. Tämän luettelon avulla voit seurata ostotilauksia, jotka voidaan laskuttaa.

### <a name="responding-to-pos"></a>Ostotilauksiin vastaaminen

Asiakkaan sinulle tarkastettaviksi lähettämät ostotilaukset näkyvät **Ostotilauksen vahvistus** -työtilassa ja **Tarkistettavat ostotilaukset** -sivulla. Kun olet avannut ostotilauksen, voit hyväksyä, hylätä tai hyväksyä ostotilauksen muutosten kera. Ostotilauksen otsikossa tai yksittäisillä riveillä voi olla liitteitä. Voit lisäksi liittää vastaukseesi tietoja ostotilauksen otsikkoon tai yksittäisille riveille. Voit esimerkiksi ehdottaa korvaavaa nimikettä yhdelle riville.

Voit esikatsella ja tulostaa ostotilauksen PDF-muodossa **Esikatselu/tulostus** -asetuksella. Voit piilottaa tai näyttää seuraavat dimensiosarakkeet **Näytä dimensiot** -toiminnolla: **Toimipaikka**, **Varasto**, **Väri**, **Koko**, **Tyyli** ja **Konfiguraatio**. 

Käytettäessä **Hyväksy muutosten kera** -vaihtoehtoa, voit hyväksyä tai hylätä yksittäisiä rivejä. Voit tehdä seuraavia muutoksia riveille:

- Päivämäärien tai määrien muuttaminen. Voit päivittää vahvistetun toimituspäivän kaikilla riveillä valitsemalla **Päivitä toimituspäivä** -asetuksen ostotilauksen otsikossa.
- Jaa rivit eri toimituspäivämäärille tai määrille.
- Korvaa nimike. Anna nimikkeen kuvaus ja nimiketunnus **Ulkoinen**-kentän **Rivin tiedot** -osassa.

Et voi muuttaa hinnoittelutietoja etkä maksuja, mutta voi tehdä niihin muutosehdotuksia käyttämällä huomautuksia.

Jos asiakas lähettää sinulle uuden version ostotilauksesta version, sen loppuliite osoittaa, että kyseessä on aiemmin lähetetyn ostotilauksen muokattu versio. Voit seurata **Ostotilausten toimittajan vahvistushistoria** -sivulla kunkin tilauksen historiatietoja.

## <a name="monitoring-consignment-inventory"></a>Tavaralähetysvaraston valvonta

Jos käytät tavaralähetysvarastoa, voit tarkastella tietoja toimittajayhteistyöliittymässä seuraavilla sivuilla:

- **Tavaralähetysvarastoa kuluttavat ostotilaukset** – Tavaralähetysvaraston ostotilaukset luodaan, kun varaston omistajuus siirtyy asiakkaalle. Nämä tavaralähetyksen ostotilaukset näkyvät vain tällä sivulla. Niitä ei ole **Kaikki vahvistetut ostotilaukset** -sivulla.
- **Tavaralähetysvarastosta vastaanotetut tuotteet** – Tällä sivulla on luettelo kaikista tapahtumista, joissa tuotteiden omistajuus siirretään varastoa kuluttavalle yritykselle. Näiden tietojen avulla voit laskuttaa asiakasta.
- **Käytettävissä oleva tavaralähetysvarasto** – Tällä sivulla on käytettävissä oleva tavaralähetysvarasto, jonka yritys omistaa mutta joka on käytettävissä asiakkaan varastossa.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Tarjouspyyntöjen käsittely Toimittajan tarjoukset -työtilassa

Voit tarkastella **Toimittajan tarjoukset** -työtilassa tarjouspyyntöjä, joihin yrityksesi on kutsuttu vastaamaan. Voit myös vastata tarjouspyyntöön. 

Työtilassa on myös kaikki hävityt ja voitetut tarjouspyynnöt. Jos järjestelmä on lisäksi määritetty julkisen sektorin käyttöön, työtilassa on julkisesti käytettävissä olevat tarjouspyynnöt.

### <a name="viewing-rfqs"></a>Tarjouspyyntöjen tarkastelu

Saat käyttöösi seuraavat tiedot avaamalla **Toimittajan tarjoukset** -työtilan:

- Kun valitset **Uudet tarjouskutsut**, näet tarjouspyynnöt, joihin yritys on kutsuttu vastaamaan. Voit tarkastella tarjouspyyntöä täällä ja aloittaa tarjousprosessin. Näet myös muunnetut tarjouspyynnöt, joihin on lähetettävä uusi tarjous.
- Kun valitset **Palautetut tarjoukset**, näet tarjouspyynnöt, jotka asiakas on palauttanut lisätietoja tai tarjouksen päivittämistä varten.
- Kun valitset **Käsittelyssä olevat tarjoukset**, näet tarjouspyynnöt, joita sinä tai yritystä edustava yhteyshenkilö on käsitellyt mutta jota ei ole vielä lähetetty.
- Kun valitset **Myönnetyt tarjoukset**, näet milloin asiakas on myöntänyt vähintään yhden tarjouksen rivinimikkeen.
- Kun valitset **Hävityt tarjoukset**, näet tarjoukset, jonka kaikki rivit on hylätty.
- Kun valitset **Tarjouspyynnöt**-linkit, näet luettelon kaikista toimittajan tarjouspyyntökutsuista ja lähetetyistä tarjouksista. **Tarjouspyynnöt**-sivulla on luettelo kaikista tarjouspyynnöistä, joissa toimittaja on ollut mukana. Voit tehdä haun tilan perusteella.
- Kun valitset **Hylätyt tarjoukset** -linkin, näet luettelon kaikista tarjouspyynnöistä, joissa toimittajan yhteyshenkilö on hylännyt tarjouksen tekemisen.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Julkisesti käytettävissä olevien tarjouspyyntöjen käsitteleminen

Julkisella sektorilla työskentelevät henkilöt näkevät julkisiksi tehdyt avoimet ja vanhentuneet tarjouspyynnöt.

- Kun valitset **Avaa julkaistut tarjouspyynnöt** -linkin, näet luettelon julkisesti käytettävissä olevista avoimista tarjouspyynnöistä. Avoimella tarjouspyynnöllä tarkoitetaan tarjouspyyntöä, joka ei ole vielä vanhentunut. Vanhentumispäivä ja -aika näkyvät tarjouspyynnön otsikossa.

    Jos sinut on kutsutte tekemään tarjous, sama tarjouspyyntö on myös **Uudet tarjouskutsut** -sivulla. Haluat ehkä joskus tehdä tarjouksen avoimelle tarjouspyynnölle, vaikka sinua ei ole kutsuttu tekemään tarjousta. Siinä tapauksessa voit ehkä kutsua itse itsesi, jos toimittaja on ottanut itsekutsumisen käyttöön tarjouspyyntötapauksessa.

    Paranna **Avaa julkaistut tarjouspyynnöt** -linkin helppokäyttöisyyttä ottamalla käyttöön **Näytä Avaa julkaistut tarjouspyynnöt -linkki ruutuna** -ominaisuus. Tämä ominaisuus muuntaa linkin ruuduksi ja siirtää sen näkyvälle paikalle, jolloin se on helppo löytää.

- Kun valitset **Suljetut julkaistut tarjouspyynnöt** -linkin, näet luettelon julkisesti käytettävissä olevista suljetuista tarjouspyynnöistä. Suljetulla tarjouspyynnöllä tarkoitetaan vanhentunutta tarjouspyyntöä. Vanhentumispäivä ja -aika näkyvät tarjouspyynnön otsikossa.

    Suljettu tarjouspyyntö näyttää kaikki toimittajien tarjoukset rivitasolle saakka. Sitä mukaan kun tarjouksia myönnetään tai hylätään, kyseinen tieto näkyy suljetussa tarjouspyynnössä. Myös tarjoukseen sisältyneet liitteet ovat käytettävissä.

> [!NOTE]
> Huomautus: tämä toiminto on käytettävissä vain, jos julkisen sektorin määritykset on otettu käyttöön.

### <a name="bidding"></a>Tarjoukset

- Aloita tarjouspyyntöön liittyvän tarjouksen tekeminen valitsemalla **Tarjous**.

    Jos tarjouspyynnön otsikon ja rivien tarjouskenttien muokkaus on otettu käyttöön, voit antaa tarjouksen suoraan riviruudukkoon. Sinun on otettava huomioon myös rivitietoihin lisättävät tarjouksen lisätiedot.

    Kun aloitat tarjouksen käsittelyn, se tulee näkyviin **Käsittelyssä olevat tarjoukset** -osaan.

    Voit tallentaa tarjouksen koska tahansa ennen vanhentumispäivää. Voit sitten palata myöhemmin viimeistelemään ja lähettämään tarjouksen. Voit peruuttaa tarjouksen ja päivittää sitä lähettämisen jälkeen vanhentumispäivään saakka.

- Voit nollata tarjoukseen annetut tiedot ja palauttaa sen alkuperäiseksi tarjouspyynnöksi valitsemalla **Nollaa arvot tarjouspyynnöstä**. Voit nollata otsikon tai rivin arvot.
- Voit käsitellä vaihtoehtoisia arvoja valitsemalla riviruudukossa **Lisää vaihtoehto** tai **Poista vaihtoehto**.

    Jotkin tarjouspyynnöt sallivat vaihtoehtoiset tarjoukset. Voit määrittää vaihtoehtotarjoukset **Luokka**-tyypin riveille, koska yksittäisiä nimikkeitä ei voi lisätä vaihtoehtoina. 

- Voit avata asiakkaan tarjouspyyntöön lisäämän liitteen valitsemalla **Tarjouspyynnön liite** tai **Tarjouspyynnön rivien liite**. Voit ladata liitteet yhdessä tarjouksen kanssa valitsemalla **Tarjouksen liitteet** tai **Tarjousrivin liitteet**.

    On mahdollista, että sinun on vastattava kyselylomakkeeseen, ennen kuin voit lähettää tarjouksen.

- Valitse **Hylkää**, jos et halua tehdä tarjousta. Kun olet valinnut **Hylkää**, ei voi peruuttaa toimintoa etkä tehdä tarjousta.

Jos tarjouspyyntöä muutetaan, sinun on tehtävä uusi tarjous. Lisätietoja muutoksesta on tarjouspyyntösivun **Muutokset**-välilehdessä. Muutettu tarjouspyyntö näkyy **Uudet tarjouskutsut** -sivulla.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Toimittajan päätietojen käyttäminen Toimittajantiedot-työtilassa

Voit toimittajana käyttää niitä tietoja, joita asiakas hallitsee toimittajan päätietueessa. Niinpä voitkin pitää tiedot ajan tasalla. Tietojen päivittäminen edellyttää, että sinulla toimittajan (ulkoinen) järjestelmänvalvojan rooli.

Käytettävissä on seuraavat tiedot: toimittajan nimi, osoitteet, yhteystiedot, yhteyshenkilöt ja heidän yhteystietonsa, tunnusnumerot, verorekisteröintinumerot, hankintaluokat, joiden myynti toimittajalta asiakkaalle on hyväksytty, sekä tiedot varmenteista.

## <a name="additional-resources"></a>Lisäresurssit

[Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]