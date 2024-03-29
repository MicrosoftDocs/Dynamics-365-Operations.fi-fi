---
title: Toimittajatilien asettaminen
description: Tässä artikkelissa kuvataan tiedot, jotka on määritettävä uutta toimittajatiliä luotaessa.
author: GalynaFedorova
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendBankAccounts, VendTable, VendOnHoldUpdate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1ddf126305f39a35f61b9a98da1c6bce29372cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875272"
---
# <a name="set-up-vendor-accounts"></a>Toimittajatilien asettaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan tiedot, jotka on määritettävä uutta toimittajatiliä luotaessa.

Luodessasi toimittajatilin, syötetään toimittajan tiedot. Näitä tietoja käytetään syöttämään tietoja asiakirjoihin automaattisesti sekä toimittajaan liittyvän toiminnan seuraamiseen. Voit esimerkiksi määrittää toimittajalle seuraavat tiedot:

-   Toimittajaryhmän määrittäminen. Jokaiselle toimittajalle on määritettävä toimittajaryhmä. Toimittajaryhmän jäsenillä on jaettuja parametreja. Niillä voi olla esimerkiksi samat maksuehdot.
-   Konfiguroi toimittaja luettelon tuontia varten Toimittajat voivat lähettää tiedoston, joka sisältää luettelon kyseisen toimittajan nimikkeistä ja palveluista. Tiedosto lähetetään järjestelmään, jotta työntekijäsi voivat tehdä tilauksia toimittajalle.
-   Toimittajan määrittäminen hankintaluokkiin.
-   Salli olemassa olevan toimittajan tehdä liiketoimintaa toisen organisaation yrityksen kanssa.
-   Aseta toimittaja pitoon tietyntyyppisille tapahtumille.
-   Määritä toimittajan pankkitiedot siten, että voit lähettää maksut sähköisesti.
-   Määritä arvonlisävero, toimitus, lasku ja toimittajan maksutiedot. Oletusarvon mukaan nämä asetukset kopioidaan uusiin toimittajalle luomiisi asiakirjoihin.
-   Määritä oletusarvoiset taloushallinnon dimensiot, joita käytetään kirjaamaan tapahtumia kirjanpitotileihin automaattisesti toimittajan kanssa.

Toimittajatilien luomisprosessia voi nopeuttaa luomalla malleja. Mallit luodaan **Toimittaja**-sivulta napsauttamalla toimintoruudussa **Asetukset** &gt; **Tietueen tiedot**. Valitse sitten **Yrityksen tilien malli**. Yrityksen tilien mallit jaetaan muille käyttäjille.  

Voit myös luoda käyttäjän mallin omaan käyttöösi. Et voi poistaa toimittajaa, joka liittyy muihin tietueisiin, kuten tuotteisiin tai yhteyshenkilöihin.

## <a name="vendor-account-numbers"></a>Toimittajan tilinumerot
Tilinumero on toimittajan yksilöivä tunnus. Voit määrittää järjestelmän luomaan tilinumerot automaattisesti, kun luot toimittajan. Numerosarjan voi myös määrittää niin, että numerot määritetään manuaalisesti. Voit esimerkiksi käyttää toimittajan puhelinnumeroa tunnuksena.

## <a name="vendor-organizations-and-individual-vendors"></a>Toimittajaorganisaatiot ja yksittäiset toimittajat
Kun luot uuden toimittajatilin, on valittava, onko toimittaja henkilö tai organisaatio. Valinta vaikuttaa tietoihin, jotka toimittajasta on määritettävä. Henkilön tietoihin kuuluvat etu- ja sukunimi sekä nimike. Organisaation tietoihin kuuluvat organisaation numero ja sen työntekijöiden määrä.

## <a name="addresses"></a>Osoitteet
Jokaiselle toimittajalle voidaan määrittää useita osoitteita, joita käytetään eri tarkoituksiin. Voit luoda osoitteen, jonka tarkoitus on **Lasku**. Tai jos suoritat maksut toimittajalle käyttämällä sekkejä, voit määrittää osoitteen, jonka tarkoitus on **Maksusuorituksen saaja**. Jos osoitetta käytetään kansainvälisissä tilisiirroissa, tarkoitus on **SWIFT**.

## <a name="vendor-contacts"></a>Toimittajan yhteyshenkilöt
Voit tallentaa toimittajalle yhteyshenkilöitä. Yhteyshenkilöitä voidaan sitten käyttää asiakirjoissa, kuten ostotilauksissa tai tarjouspyynnöissä.  

Toimittajan yhteyshenkilöitä voit lisätä **Kaikki toimittajat** -sivulla, napsauttamalla **Toimittaja**-välilehden **Asetukset**-ryhmässä **Yhteyshenkilöt** &gt; **Lisää yhteyshenkilöitä**.  

Voit luoda uuden toimittajan alusta alkaen. Vaihtoehtoisesti, voit kopioida tiedot toisesta henkilöstä, joka on jo rekisteröity Supply Chain Managementiin, ja muokata tietoja tarvittaessa.  

**Huomautus:** Yhteyshenkilön lisääminen toimittajalle ei ole sama asia kuin toimittajan yhteystietojen lisääminen. Vaikka voitkin lisätä toimittajalle yleisiä yhteystietoja, sinulla voi myös olla useita, tiettyjä henkilöitä, jotka ovat yhteyshenkilöitäsi kyseisessä yrityksessä, ja kaikilla heillä on omat yhteystietonsa.  

Et voi poistaa yhteyshenkilötietuetta, jos yhteyshenkilöön viitataan asiakirjassa. Sen sijaan voit poistaa yhteyshenkilön aktivoinnin.  

Voit lisätä toimittajan yhteyshenkilöitä omiin Microsoft 365 -yhteystietoihisi. Sinun on kuitenkin ensin määritettävä Supply Chain Managementin ja Microsoft 365:n välinen synkronointi sekä Microsoft Exchange Serverin synkronoinnissa että ohjatussa Microsoft Outlook -asennustoiminnossa.

## <a name="vendors-in-different-legal-entities"></a>Toimittajat eri yrityksissä
Jos toimittaja on rekisteröity vain yhteen yritykseen organisaatiossasi ja toisen yrityksen on rekisteröitävä sama toimittaja, voit käyttää **Lisää toimittaja toiseen yritykseen** -sivun avulla, jossa voit määrittää toimittajalle liikesuhteen toisen yrityksen kanssa. Sinun on valittava toimittajalle toimittajaryhmä, valuutta ja pidon tila valitussa yrityksessä.  

Jos organisaatiossasi on useita yrityksiä, jotka toimivat saman toimittajan kanssa, ja jos kukin yritys ylläpitää erillistä toimittajatiliä kyseistä toimittajaa varten, voit näiden ohjeiden avulla yhdistää eri toimittajatilit. Näin osoite- ja työntekijöiden määrätiedot voidaan jakaa siten, että ne on päivitettävä vain yhdessä paikassa.  

Voit yhdistää osapuolten tunnukset seuraavien ohjeiden mukaisesti.

1.  Avaa **Yleinen osoitekirja** -sivu ja valitse osoitekirjatietueet, jotka edustavat toimittajaa kussakin yrityksessä, jotka haluat sisällyttää määritykseen.
2.  Valitse Toimintoruudussa **Yhdistä tietueet**.

## <a name="agreements"></a>Sopimukset
Kun määrität toimittajatilin, voi myös olla hyvä rekisteröidä toimittajan kanssa solmitut sopimukset. Toimittajatietueen toimintojen avulla voit määrittää hinta- ja alennussopimukset. Voit myös määrittää ostosopimuksen **Ostosopimukset**-sivulla.

## <a name="putting-a-vendor-on-hold"></a>Toimittajan asettaminen pitoon
Voit asettaa toimittajan pitoon eri tapahtumatyyppien kohdalla. Valittavissa ovat seuraavat vaihtoehdot:

-   **Ei** – Toimittaja ei ole pidossa.
-   **Lasku**– Laskuja ei voi luoda tai kirjata toimittajalle.
-   **Kaikki** - Toimittajan kaikki tapahtumatyypit ovat pidossa. Tapahtumatyypit sisältävät ostoehdotukset, laskut ja maksut.
-   **Maksu** – Maksuja ei voi luoda toimittajalle.
-   **Ehdotus** – Ostoehdotuksia ei voi luoda toimittajalle, ja hankintarivejä, jotka on jo luotu ennen toimittajan estossa-asetusten muuttamista, ei voi muuntaa ostotilaukseksi. Toimittajan ehdotusrivit peruutetaan, jos käytäntö on määritetty luomaan ostotilaukset automaattisesti.
-   **Ei koskaan** – Toimittajaa ei aseteta pitoon aktiivisuuden puutteen vuoksi.

Kun asetat toimittajan pitoon, voit myös määrittää pidolle syyn ja päivämäärän, jona pitotila päättyy. Jos et määritä päättymispäivämäärää, toimittajan pitotila on voimassa toistaiseksi.

Voit joukkopäivittää toimittajan pidossa-tilan tilaan **Kaikki** **Toimittajan inaktivointi** -sivulla valittujen ehtojen perusteella ja määrittää, miksi toimittaja on pidossa.

Seuraavilla ehdoilla sisällytetään toimittajat, jotka ovat olleet kaudella passiivisia, sisällyttää tai sulkea pois toimittajat, jotka ovat työntekijöitä, ja sulkea pois toimittajat, joilla on lisäaikaa ennen seuraavaa pitoa.

- Sovellus laskee **Toimittajan inaktivointi** -sivun **Pitojakso**-kenttään annettujen päivien perusteella viimeisen päivän, jolloin toimittajalla voi olla tehtäviä, jotta toimittaa ei pidettäisiä aktiivisena. Toisin sanoa kuluva päivä, josta on vähennetty annettujen päivien määrä. Jos toimittajalla on ainakin yksi lasku, jossa päivämäärä laskettua viimeisintä päivämäärää myöhäisempi, toimittaja jätetään pois inaktivoinnista. Tämä tarkistetaan myös, jos toimittajalla on maksuja kyseisen päivämäärän jälkeen, avoimia ostoehdotuksia, avoimia ostotilauksia, tarjouspyyntöjä tai vastauksia.
- **Lisäaika ennen seuraavaa pitoa** -kentässä olevaa päivien määrää käytetään laskemaan lisäajan viimeinen päivä. Toisin sanoa kuluva päivä, josta on vähennetty antamasi päivät. Tämä koskee vain toimittajia, jotka on inaktivoitu aiemmin. Jos kyse on aiemmasta inaktivoinnista, sovellus varmistaa, onko toimittajalla muita inaktivointeja, ja tarkistaa, tapahtuiko viimeisin inaktivointi ennen lisäajan viimeistä päivää. Jos näin on, toimittaja sisällytetään inaktivointiprosessiin.
- Parametri **Sisältää työntekijät** viittaa työntekijään linkitettyihin toimittajiin. Voit määrittää sen, jos haluat sisällyttää kyseiset työntekijät.

Prosessi sulkee aina pois toimittajat, joiden arvo **Toimittajan pito** -kentässä on **Ei koskaan**.

Tarkistukset läpäisevät toimittajat asetetaan pitoon, jolloin **Toimittajan pito** -kentän arvoksi tulee **Kaikki** ja **Syy** valinnalle. Toimittajalle luodaan tietue pitohistoriaan.

## <a name="vendor-invoice-account"></a>Laskutustoimittaja
Jos usealla toimittajalla on sama laskutusosoite tai jos toimittajaa laskutetaan kolmannen osapuolen kautta, voit määrittää toimittajatietueelle erillisen laskutustilin. Laskutustili on tili, jota hyvitetään laskun summalla, kun toimittajalasku luodaan ostotilauksesta. Jos laskutustiliä ei luoda toimittajan tietueelle, laskutustilinä käytetään toimittajatiliä.

## <a name="vendor-bank-accounts"></a>Toimittajan pankkitilit
Jos suoritat maksuja toimittajan pankkitilille, voit syöttää toimittajan pankki- ja pankkitilitiedot **Toimittajan pankkitilit**-sivulla. Voit myös kirjoittaa valitun pankkitilin oikeellisuustarkistus- ja maksutiedot. Voit esimerkiksi lisätä esilaskuja toimittajan pankkitileille. Näitä esilaskuja voi käyttää tilitietojen, kuten reititysnumeroiden ja tilinumeroiden, oikeellisuuden tarkastamiseen. Toimittajalle on määritettävä oletusmaksutili. Varsinaista maksua suoritettaessa tämän tilin voi muuttaa joksikin toiseksi toimittajan tiliksi.

## <a name="ledger-accounts"></a>Kirjanpitotilit
Voit määrittää oletustilit, jotka näkyvät automaattisesti toimittajan laskujen kirjauskansioissa määritetyn toimittajan osalta. Tämä toiminnallisuus voi olla hyödyllinen, jos yleensä maksat samantyyppisistä nimikkeistä tai palveluista samoille toimittajille ajan kuluessa. Kun määrität oletustilin, voit nopeasti ja tehokkaasti määrittää kirjauskansiomerkinnät laskukirjauskansioon. Määritettäviä oletustilejä ei käytetä ostotilauksille tai toimittajalaskuille, jotka on kirjataan **Toimittajalasku**-sivulla.  

Oletustilit valitaan **Oletustilin määritys** -sivulla, jonka voit avata toimittajatietueen **Lasku**-välilehdeltä. Tässä valitut tilit näkyvät suodatetussa toimittajatilien luettelossa, kun kirjaat kirjauskansioviennin. Yhden tileistä voi määrittää oletustiliksi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]