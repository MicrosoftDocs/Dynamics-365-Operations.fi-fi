---
title: Ostosopimukset
description: Tässä artikkelissa on tietoja ostosopimuksista. Ostosopimus on sopimus, joka velvoittaa organisaation ostamaan tietyn määrän tai tietyllä summalla, käyttämällä useita ostotilauksia jonkin ajanjakson aikana. Vastineeksi tästä sitoumuksesta, ostaja saa erityiset hinnat ja alennukset.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a8e2c4fdf640f1a9a64c60afc978a4d5812182a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669542"
---
# <a name="purchase-agreements"></a>Ostosopimukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja ostosopimuksista. Ostosopimus on sopimus, joka velvoittaa organisaation ostamaan tietyn määrän tai tietyllä summalla, käyttämällä useita ostotilauksia jonkin ajanjakson aikana. Vastineeksi tästä sitoumuksesta, ostaja saa erityiset hinnat ja alennukset. 

Ostosopimukset voivat koskea tiettyä määrää tuotetta, tietyn tuotteen valuuttasummaa tai tiettyjen tuotteiden valuuttasummaa hankintaluokassa. Ostosopimuksen hinnat ja alennukset ohittavat muut hinnat ja alennukset, jotka on määritelty missään kauppasopimuksissa, jotka ovat jo olemassa.  

Voit luoda, hakea ja seurata **Ostosopimukset**-sivulla ostosopimuksia, jotka ovat voimassa oman organisaatiosi ja toimittajien välillä. Esimerkiksi, kun olet luonut ostosopimuksen, voit tilata suoraan siitä. Kaikilla ostosopimuksilla on voimassaoloaika, jonka määrää se henkilö, joka luo ostosopimuksen. Hankinnan toimitusajan on sijoituttava tämän voimassaoloajan päivämäärävälille.  

Kun olet luonut ostosopimuksen, se tulee voimaan vasta, kun se on aktivoitu. Aktivoi ostosopimus valitsemalla **Merkitse sopimus voimassa olevaksi** -asetukseksi **Kyllä**. 

Voit estää ostosopimuksen käytön ja vahvistamisen merkitsemällä sopimuksen tilaksi **suljettu.** Voit silti päivittää tilaksi **Voimassa** milloin tahansa tämän muutoksen tekemisen jälkeen.

## <a name="responsible-workers-on-purchase-agreements"></a>Ostosopimuksista vastaavat työntekijät

Voit määrittää ensisijaisen vastuullisen työntekijän ja toissijaisen vastuullisen työntekijän ostosopimuksen luokittelussa. Nämä arvot periytyvät tuloksena olevasta ostosopimuksesta. Sinun ei tarvitse lisätä vastuullisia työntekijöitä ostosopimukseen, ja niitä voidaan muokata suoraan tapauskohtaisesti ostosopimuksen perusteella. Et voi määrittää toissijaista vastuutyöntekijää ilman ensisijaista vastuullista työntekijää, vaikka sinulla ei ole toissijaista vastuutyöntekijää. Et voi määrittää samaa työntekijää sekä ensisijaiseksi että toissijaiseksi vastuulliseksi työntekijäksi.

> [!IMPORTANT]
> Jotta voit käyttää vastuullinen osapuoli -toimintoa, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus oletusarvoisesti käytössä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Ostosopimuksen vastuullinen osapuoli* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="commitment-types"></a>Vahvistustyypit
Jokainen rivi ostosopimuksessa velvoittaa ostamaan jotakin. Voit täyttää sitoumuksen käyttämällä useiden ostotilausten rivejä. On neljänlaisia sitoumuksia:

-   **Tuotteen määrän vahvistus** – ostat tietyn määrän tuotteita.
-   **Tuotteen arvoon perustuva sitoumus** – ostat tuotetta tietyllä valuuttasummalla.
-   **Tuoteluokan arvon sitoutuminen** - Ostat tietyllä valuuttasummalla hankintaluokasta. Summa voi olla luetteloartikkelille tai artikkelille muualta kuin luettelosta.
-   **Arvon sitoutuminen** – ostat tietyllä valuuttasummalla tuotteita jostain hankintaluokasta.

## <a name="pricing-terms-for-purchase-agreements"></a>Ostosopimusten hintaehdot
Hintaehdot voivat olla erilaisia, riippuen sitoumustyypistä. Ostosopimusten hintaehdot ohittavat muut hintaehdot, jotka on määritelty kauppasopimuksille. Seuraava taulukko kuvailee hintoihin liittyvät kentät, joihin eri sitoumustyypit vaikuttavat. Kentät joissa on **Kyllä** voidaan päivittää tilausrivillä.

| Vahvistustyyppi                   | Yksikköhinta | Hintayksikkö | Alennusprosentti | Käteisalennussumma |
|-----------------------------------|------------|------------|------------------|----------------------|
| Tuotteen määrän vahvistus       | Kyllä        | Kyllä        | Kyllä              | Kyllä                  |
| Tuotteen arvon vahvistus          |            |            | Kyllä              |                      |
| Tuoteluokan arvon sitoutuminen |            |            | Kyllä              |                      |
| Arvon sitoutuminen                  |            |            | Kyllä              |                      |

## <a name="policies-for-purchase-agreements"></a>Ostosopimusten säännökset
Seuraavat käytännöt vaikuttavat siihen, miten ostosopimussitoumuksen ja sitä vastaavien ostotilausrivien välinen yhteys toimii:

-   **Maksimi pakotetaan** – Kaikkien tilausrivien kokonaismäärä tai summa ei voi olla enempää kuin sitä vastaavan sitoumuksen määrä tai summa.
-   **Hinta ja alennus on kiinteä** – Tilausrivin ja sitä vastaavan sitoumuksen hinnan on oltava sama. Jos tilausrivin hintaa muutetaan, yhteys sitoumukseen rikkoutuu. Jos yhteys katkeaa, tilausrivi ei edistä sitoumuksen täyttymistä.
-   **Vapautuksen vähimmäissumma ja Vapautuksen enimmäissumma** – Jos summa on määritetty, saat ilmoituksen, jos yrität tehdä tilausriviin muutoksia, joiden seurauksena tilausrivi poikkeaa siihen liittyvästä sitoumuksesta.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Ostosopimusten toteutumisen laskelmoinnit
**Ostosopimukset**-sivun **Rivin tiedot** -pikavälilehdessä olevassa **Täytäntöönpano**-välilehdessä näkyvät täytäntöönpanon määrät ja summat.  

Sitoumuksen täytäntöönpanoon tarvittavat jäljellä oleva summa tai määrä näkyy **Täytäntöönpano**-alueella.  

**Sopimus**-alueella näkyy kokonaismäärä tai kokonaissumma, jolla myyntisopimusrivi on voimassa.  

Voit käyttää täytäntöönpanon laskentaan vaikuttavia ostotilausrivejä ja laskurivejä valitsemalla **Liittyvät tiedot** -toiminnon ostosopimuksen riveillä tai otsikossa.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Ostosopimusten vahvistukset ja versiohistorian
Kun vahvistat ostosopimuksen, sen uusin versio tallennetaan historiataulukkoon. Jos muutat ostosopimusta, voit vahvistaa sen uudestaan tallentaaksesi toisen ostosopimuksen version historiaan. Jos et vahvista ostosopimusta, voit yhä luoda ostotilauksia sen pohjalta. Mutta ostosopimusten historiatietoja ei säilytetä. Voit esikatsella tai tulostaa kaikki sopimuksen versiot. Sitten voit jakaa korjaukset toimittajasi kanssa saadaksesi hyväksynnän.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Ostosopimukset lisääminen tilausprosessiin
Kun luot ostotilauksen, voit käyttää siinä ostosopimusta. Sopimusehtojen tiedot, kuten maksuehdot, toimitusajat ja toimitusosoite, kopioidaan sitten ostotilauksen otsikkoon. Jos ostotilauksessa on vähintään yksi sopimuksen kattaman tuotteen tai luokan rivi, kyseisillä riveillä käytetään ostosopimuksen hintoja ja alennuksia. Tilausrivin summa tai määrä vaikuttaa ostosopimuksen sitoumuksen täytäntöönpanoon. Sama ostotilaus voi sisältää sekä rivejä, jotka eivät liity ostosopimukseen, että rivejä, jotka ovat sitoutuneet ostosopimukseen.  

Voit valita ostosopimuksen vain, kun olet luomassa ostotilausta. Et voi valita ostosopimusta, kun ostotilaus on luotu.  
Joissakin tilanteissa, joissa ostotilaukset luodaan epäsuorasti, voit määrittää, hakeeko Supply Chain Management automaattisesti käytettävää ostosopimusta. Voit esimerkiksi toimia näin, kun vahvistat automaattisesti suunniteltuja ostotilauksia tai luot ostotilauksia, jotka perustuvat myyntitilauksiin.

## <a name="matching-policy-on-purchase-agreements"></a>Ostosopimusten vastaavuuskäytäntö
Voit määrittää rivin vastaavuuskäytännön ostosopimuksen otsikossa. Tämä rivin vastaavuuskäytäntö noudattaa ostoreskontran parametrien rivin vastaavuuskäytäntöä, kun **Ostoreskontran parametrit** -sivun (**Hinnan ja määrän täsmäytys** -pikavälilehden) **Salli vastaavuuskäytännön ohitus** -kentän asetuksena on **Yrityksen käytäntöä suurempi**. Ostosopimukseen viittaavat asiakirjat käyttävät ostosopimuksen otsikossa määritettyä vastaavuuskäytäntöä, ellei vastaavassa nimikkeessä, nimikkeessä ja toimittajassa tai luokan ostokäytännössä ole määritetty jotain muuta.

## <a name="purchase-agreements-and-intercompany-trade"></a>Ostosopimukset ja konsernin sisäinen kauppa
Yhtiöiden väliset jäljityssuhteet voidaan luoda toimittajan tilien ja asiakkaan tilien välille, kun ne ovat eri oikeushenkilöitä. Kun myyntitilaus tai ostotilaus luodaan yhdelle osapuolelle, luodaan myös konsernin sisäinen tilausketju. Tilausketjussa myyntitilaus ja ostotilaus on luotu soveltuville yrityksille.  

Voit luoda ostosopimuksen tai myyntisopimuksen yhdelle yhtiöiden väliselle kaupankäynnin osapuolelle. Sitten voit kehittää vastaavan ostosopimuksen tai myyntisopimuksen toiselle yhtiöiden väliselle kaupankäynnin osapuolelle toisessa laillisessa kokonaisuudessa.  

Jos luot konsernin sisäisen ostosopimuksen, joka käyttää konsernin sisäistä ostosopimusta yhdessä yrityksessä, vastaava konsernin sisäinen myyntitilaus käyttää vastaavaa konsernin sisäistä myyntisopimusta toisessa yrityksessä. Myyntisopimuksen sitoumuksien täytäntöönpano ja ostosopimusten täytäntöönpano on synkronoitu samalla tavoin kuin konsernin sisäinen myyntitilaus ja konsernin sisäinen ostotilaus on synkronoitu.

## <a name="financial-dimensions-on-purchase-agreements"></a>Ostosopimusten taloudelliset dimensiot
Voit kopioida taloudelliset dimensiot asiakirjojen ylätunnisteisiin tai ostosopimusten yksittäisille riveille. Jos muutat sopimuksen otsikon tai sopimusrivin dimensioita, muutos ei vaikuta vapautettuihin tilauksiin mutta sitä käytetään uusissa tilauksissa.

## <a name="additional-resources"></a>Lisäresurssit

- [Ostosopimuksen luominen](tasks/create-purchase-agreement.md)
- [Ostosopimuksen käyttö ostotilausta luotaessa](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]