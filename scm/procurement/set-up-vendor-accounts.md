---
title: Toimittajatilien asettaminen
description: "Tässä aiheessa kuvataan tiedot, jotka on määritettävä uutta toimittajatiliä luotaessa."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendBankAccounts, VendTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4c97f11fa85b8eee54daea8ccaa183859a89fe7f
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-vendor-accounts"></a>Toimittajatilien asettaminen

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan tiedot, jotka on määritettävä uutta toimittajatiliä luotaessa.

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

Voit luoda uuden toimittajan alusta alkaen. Vaihtoehtoisesti, voit kopioida tiedot toisesta henkilöstä, joka on jo rekisteröity Microsoft Dynamics 365 for Finance and Operations -järjestelmään ja muokata tietoja tarpeen mukaisesti.  

**Huomautus:** Yhteyshenkilön lisääminen toimittajalle ei ole sama asia kuin toimittajan yhteystietojen lisääminen. Vaikka voitkin lisätä toimittajalle yleisiä yhteystietoja, sinulla voi myös olla useita, tiettyjä henkilöitä, jotka ovat yhteyshenkilöitäsi kyseisessä yrityksessä, ja kaikilla heillä on omat yhteystietonsa.  

Et voi poistaa yhteyshenkilötietuetta, jos yhteyshenkilöön viitataan asiakirjassa. Sen sijaan voit poistaa yhteyshenkilön aktivoinnin.  

Voit lisätä toimittajan yhteyshenkilöitä omiin Microsoft Office 365 -yhteystietoihisi. Sinun on kuitenkin ensin määritettävä Dynamics 365 for Finance and Operationsin ja Office 365:n välinen synkronointi sekä Microsoft Exchange Serverin synkronoinnissa että ohjattu Microsoft Outlook -asennustoiminnossa.

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
-   **Ostoehdotus** – Vain ostoehdotuksia voidaan luoda toimittajalle. Muita tapahtumia ei voi luoda.
-   **Ei koskaan** – Toimittajaa ei aseteta pitoon aktiivisuuden puutteen vuoksi.

Kun asetat toimittajan pitoon, voit myös määrittää pidolle syyn ja päivämäärän, jona pitotila päättyy. Jos et määritä päättymispäivämäärää, toimittajan pitotila on voimassa toistaiseksi.

## <a name="vendor-invoice-account"></a>Laskutustoimittaja
Jos usealla toimittajalla on sama laskutusosoite tai jos toimittajaa laskutetaan kolmannen osapuolen kautta, voit määrittää toimittajatietueelle erillisen laskutustilin. Laskutustili on tili, jota hyvitetään laskun summalla, kun toimittajalasku luodaan ostotilauksesta. Jos laskutustiliä ei luoda toimittajan tietueelle, laskutustilinä käytetään toimittajatiliä.

## <a name="vendor-bank-accounts"></a>Toimittajan pankkitilit
Jos suoritat maksuja toimittajan pankkitilille, voit syöttää toimittajan pankki- ja pankkitilitiedot **Toimittajan pankkitilit**-sivulla. Voit myös kirjoittaa valitun pankkitilin oikeellisuustarkistus- ja maksutiedot. Voit esimerkiksi lisätä esilaskuja toimittajan pankkitileille. Näitä esilaskuja voi käyttää tilitietojen, kuten reititysnumeroiden ja tilinumeroiden, oikeellisuuden tarkastamiseen. Toimittajalle on määritettävä oletusmaksutili. Varsinaista maksua suoritettaessa tämän tilin voi muuttaa joksikin toiseksi toimittajan tiliksi.

## <a name="ledger-accounts"></a>Kirjanpitotilit
Voit määrittää oletustilit, jotka näkyvät automaattisesti toimittajan laskujen kirjauskansioissa määritetyn toimittajan osalta. Tämä toiminnallisuus voi olla hyödyllinen, jos yleensä maksat samantyyppisistä nimikkeistä tai palveluista samoille toimittajille ajan kuluessa. Kun määrität oletustilin, voit nopeasti ja tehokkaasti määrittää kirjauskansiomerkinnät laskukirjauskansioon. Määritettäviä oletustilejä ei käytetä ostotilauksille tai toimittajalaskuille, jotka on kirjataan **Toimittajalasku**-sivulla.  

Oletustilit valitaan **Oletustilin määritys** -sivulla, jonka voit avata toimittajatietueen **Lasku**-välilehdeltä. Tässä valitut tilit näkyvät suodatetussa toimittajatilien luettelossa, kun kirjaat kirjauskansioviennin. Yhden tileistä voi määrittää oletustiliksi.




