---
title: "Konsernin sisäinen laskutus"
description: "Tässä artikkelissa on tietoja ja esimerkkejä laskuttamisesta konsernin sisäisten projektien Microsoft Dynamics-365 operaatioille."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 8a606f81e6e66390bf0add3deeeb032ab4cbd90b
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-invoicing"></a>Konsernin sisäinen laskutus

Tässä artikkelissa on tietoja ja esimerkkejä laskuttamisesta konsernin sisäisten projektien Microsoft Dynamics-365 operaatioille.

Organisaatiossasi saattaa olla useita divisioonia, tytäryhtiöitä ja muita yrityksiä, jotka siirtävät tuotteita ja palveluita keskenään projekteissa. Yritys, joka tarjoaa palvelu tai tuote on nimeltään *lainaus yrityksen*, ja yritys, joka vastaanottaa palvelu tai tuote on nimeltään *lainaava yritys*. 

Seuraavassa kuvassa on tyypillinen skenaario, jossa kaksi yritystä, SI FR (lainaava yritys) ja SI USA (lainaajayritys) jakavat resurssit toimittaakseen projektin asiakkaalle A. Tässä skenaariossa SI FR on tehnyt sopimuksen työn suorittamisesta asiakkaalle A. 

[![Konsernin Laskutus-Esimerkki](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Tavoitteena on tehdä kustannusseuranta, tuottokirjausta, verot ja siirtohinta konsernin projektitapahtumien entistä joustavampia ja tehokkaampia. Lisäksi käytössä on seuraavat toiminnot:

-   Luo projektille myyntilaskuja lainaavassa yrityksessä käyttämällä lainaajayrityksessä konsernin sisäisiä aikaraportteja, kuluja ja toimittajan laskuja.
-   Tue verolaskelmia ja välillisiä kustannuksia.
-   Lykkää tuottokirjausta lainaajayrityksessä ja ajankohtaa, jolloin lainaavan yrityksen on kirjattava kustannus.
-   Jaksota keskeneräisen työn (KET) tuotto lainaajayrityksessä.
-   Määritä siirtohinnat, jotka voivat perustua eri hinnoittelumalleihin. Seuraavassa on muutamia esimerkkejä:
    -   **Määrä** – **Hinnoittelu**-kentässä annettu summa on määrä- tai yksikkökohtainen toteutunut kustannus.
    -   **Kulujen summa** – **Hinnoittelu**-kentässä annettu tapahtumakohtainen hinta/kustannus sekä kulusumma.
    -   **Kuluprosentti** – **Hinnoittelu**-kentässä annettu siirtohinta on tapahtumakohtainen hinta/kustannus kerrottuna kuluprosentilla.
    -   **Prosenttia myyntihinnasta** – lainaajayritykseen siirretty myyntihinnan prosenttiosuus.
    -   **Myyntihinnan alittava summa** – summa, jonka lainaava yritys pidättää myyntihinnasta ennen siirtoa lainaajayritykseen.
    -   **Kateprosentti**– **Hinnoittelu**-kentässä annettu luku on kateprosentti, joka ilmaistaan myyntihinnan prosenttiosuutena.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Esimerkki 1: Määritä konsernin sisäiset laskutusparametrit
Tässä esimerkissä USSI on lainaajayritys ja sen resurssit raportoivat ajan lainaavalle yritykselle, FRSI:lle, jolla on sopimus loppuasiakkaan kanssa. USSI:n työntekijöiden raportoimat tunnit ja kulut voidaan sisällyttää FRSI:n luomaan projektilaskuun. Tapahtumilla on lisäksi kolmas lähde, joka on peräisin lainaajayrityksestä (tässä esimerkissä USSI), kun se toimittaa jaettuja toimittajapalveluita tytäryhtiöille (kuten FRSI:lle) ja välittää sitten nämä kulut näiden tytäryhtiöiden projekteihin. Työvaiheiden 365 Dynamics suorittaa laskun kaikki vastaavat asiakirjat ja palveluverokoodia. 

Tässä esimerkissä FRSI:n on oltava USSI-yrityksen asiakas ja USSI:n on oltava FRSI-yrityksen toimittaja. Voit sitten määrittää konsernin sisäisen suhteen kahden yrityksen välille. Seuraavassa menettelyssä kuvataan parametrien määrittäminen siten, että kumpikin yritys voi osallistua konsernin sisäiseen laskutukseen.

1.  Määritä FRSI asiakkaaksi USSI-yritykseksi ja USSI FRSI-yrityksen toimittajaksi. Tämän tehtävän edellyttämille vaiheille on kolme aloituskohtaa.
    | Vaihe | Tulopaikka                                                                       | kuvaus   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | A    | USSI, valitse **myynti**&gt;**asiakkaiden**&gt;**kaikille asiakkaille**. | Luo FRSI:lle uusi asiakastietue ja valitse asiakasryhmä.                                                                                                                                                                                                                           |
    | B    | Valitse FRSI, **Ostoreskontra**&gt;**toimittajat**&gt;**kaikkien toimittajien**.        | Luo USSI:lle uusi toimittajatietue ja valitse toimittajaryhmä.                                                                                                                                                                                                                               |
    | K    | Avaa FRSI:ssä juuri luomasi toimittajatietue.                            | Valitse toimintoruudun **Yleiset**-välilehdessä **Määritä**-ryhmässä **Konsernin sisäinen**. Siirrä **Konsernin sisäinen** -sivun **Kauppakumppanuus**-välilehden **Aktiivinen**-liukusäädin **Kyllä**-asentoon. Valitse **Asiakasyritys**-kentässä vaiheessa A luotu asiakastietue. |

2.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**projektin kirjanpidon parametrien**, ja valitse sitten **konsernin** välilehti. Parametrien määritystapa määräytyy sen mukaan, onko kyse lainaavasta yrityksestä vai lainaajayrityksestä.
    -   Jos olet lainaava yritys, valitse hankintaluokka, jolla automaattisesti luodut toimittajan laskut täsmäytetään.
    -   Jos olet lainaajayritys, valitse kullekin lainaavalle yritykselle oletustuoteluokka kullekin tapahtumatyypille. Tuoteluokkia käytetään verojen määritykseen, kun konsernin sisäisten tapahtumien laskutettu luokka on luotu vain lainaavaan yritykseen. Voit valita konsernin sisäisten tapahtumien tuoton jaksotuksen. Jaksotus tehdään, kun tapahtumat kirjataan, ja palautetaan, kun konsernin sisäinen lasku kirjataan.

3.  Valitse **projekti, projektinhallinta- ja**&gt;**asennus**&gt;**hinnat**&gt;**siirtohinta**.
4.  Valitse valuutta, tapahtuman tyyppi ja siirtohintamalli. Laskussa käytetty valuutta on valuutta, joka on määritetty lainaajayrityksen lainaavan yrityksen asiakastietueessa. Valuuttaa käytetään täsmäyttämään viennit siirtohintataulussa.
5.  Valitse **kirjanpidon**&gt;**kirjausasetukset**&gt;**konserniyritysten välisen laskennan**, ja määrittää USSI ja FRSI suhteen.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Esimerkki 2: Luo ja kirjaa konsernin sisäinen aikaraportti
USSI:n, lainaajayrityksen, on luotava ja kirjattava FRSI:n, lainaavan yrityksen, projektin aikaraportti. Tämän tehtävän edellyttämille vaiheille on kaksi aloituskohtaa.

| Vaihe | Tulopaikka                                                                       | kuvaus                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekti, projektinhallinta- ja**&gt;**tuntilomakkeiden**&gt;**kaikki tuntilomakkeet** | Luo uusi aikaraportti. Valitse aikaraporttirivin **Yritys**-kentässä **FRSI**. Valitse **Projektitunnus**-kentässä FRSI:n projekti. Anna kunkin viikonpäivän tunnit. |
| B    | **Työaikaraportti**-sivu                                                                | Kirjaa aikaraportti työnkulun suorittamisen jälkeen ja kirjaa tositenumero muistiin.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Esimerkki 3: Luo ja kirjaa konsernin sisäinen toimittajan lasku
USSI:n, lainaajayrityksen, on luotava ja kirjattava FRSI:n, lainaavan yrityksen, projektin konsernin sisäinen toimittajan lasku. Tämä toimittajan lasku kuvaa ulkoistettua työtä ja kuluja, jotka USSI:n maksamat toimittajat suorittivat. Tämän tehtävän edellyttämille vaiheille on kaksi aloituskohtaa.

| Vaihe | Tulopaikka                                                                                      | kuvaus                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostovelat**&gt;**laskut**&gt;**avoimet toimittajalaskut**&gt;**uusi toimittajalasku** | Luo uusi toimittajan lasku ja vie FRSI-projektin puolesta hankitut palvelut.                                                                                                                                                                                  |
| B    | **Toimittajan lasku** -sivu                                                                      | Anna rivit, jotka kuvaavat FRSI:n ulkoistettuja palveluja. Lisää **Rivin erittely** -pikavälilehden laskurivin **Projekti**-välilehden **Projektiyritys**-kenttään **FRSI**. Anna projektitiedot ja muut vastaavat tiedot. Kirjaa sitten toimittajan lasku. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Esimerkki 4: Luo ja kirjaa konsernin sisäinen lasku
Lainaajayritys USSI:n on luotava ja kirjattava konsernin sisäinen lasku. Tämän tehtävän edellyttämille vaiheille on kaksi aloituskohtaa.

| Vaihe | Tulopaikka                                                                                             | kuvaus                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projekti, projektinhallinta- ja**&gt;**projektin laskujen**&gt;**konsernin sisäinen myyntilasku**  | Avaa **Luo konsernin sisäinen lasku** -sivu valitsemalla **Uusi**.                                                                                  |
| B    | **Projekti, projektinhallinta- ja**&gt;**projektin laskujen**&gt;**asiakkaan laskuihin** | Anna **Luo konsernin sisäisen lasku** -sivulla yritys, määritä sisällytettävä tapahtuma ja valitse sitten **Hae**. |
| K    | **Projekti, projektinhallinta- ja**&gt;**projektin laskujen**&gt;**asiakkaan laskuihin** | Valitse laskutettavat tapahtumat tai valitse **Valitse kaikki**, jos haluat laskuttaa kaikki luettelon tapahtumat, ja valitse sitten **OK**.                  |
| D    | **Konsernin sisäinen lasku** -sivu                                                                       | Kuvassa on konsernin sisäinen myyntilaskuehdotus.                                                                                             |
| E    | **Konsernin sisäinen lasku** -sivu                                                                       | Valitse **Kirjaa**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Esimerkki 5: Kirjaa toimittajan lasku ja laskuta asiakasta
Kun lainaajayritys USSI Kirjaa konsernin sisäisen myyntilaskun, vastaava odottava toimittajan lasku luodaan lainaavassa yrityksessä FRSI. Kun tämä toimittajan lasku on kirjattu, FRSI laskuttaa projektin asiakkaalta myös USSI:n lisäämät tunnit. Tämän tehtävän edellyttämille vaiheille on kolme aloituskohtaa.

| Vaihe | Tulopaikka                                                                                        | kuvaus                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Ostovelat**&gt;**laskut**&gt;**odottavia toimittajalaskuja**                            | Tarkista laskusta, että aikaraportin arvot ovat mukana laskussa, ja kirjaa sitten toimittajan lasku.                  |
| B    | **Projekti, projektinhallinta- ja**&gt;**projektin laskujen**&gt;**projektin laskuehdotukset** | Luoda projektille uusi projektilasku ja tarkista, että kirjatut tuntitapahtumat ovat näkyvissä.            |
| K    | **Projektilasku**-sivu                                                                       | Valitse ensin projektilasku ja tarkista sitten kustannus- ja myyntisumma valitsemalla **Näytä tiedot**. Kirjaa sitten lasku. |




