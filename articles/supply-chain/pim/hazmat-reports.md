---
title: Vaarallisten aineiden kyselyt ja raportit
description: Tässä ohjeaiheessa käsitellään erilaisten vaarallisiin aineisiin liittyvien raporttien käyttämistä. Monet näistä raporteista ovat pakollisia, sillä niiden avulla voidaan osoittaa, että lähetyksen ja säilytyksen aikana on noudatettu vaarallisia aineita koskevia määräyksiä.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 1bb96d117eb3bb2b54be1a376c8789ad73d5fec8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983363"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Vaarallisten aineiden kyselyt ja raportit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää erilaisia vaarallisiin aineisiin liittyviä raportteja. Monet näistä raporteista ovat pakollisia, sillä niiden avulla voidaan osoittaa, että lähetyksen ja säilytyksen aikana on noudatettu vaarallisia aineita koskevia määräyksiä.

**Multimodaaliset vaaralliset tavarat** -raporttia lukuun ottamatta kaikissa raporteissa käytetään lähetykselle määritettyä toimitustapaa etsimään määräys, jota on käytettävä nimikkeiden lähetystekstin tulostamiseen. Toimitustapa liitetään lähetyksen rahdinkuljettajaan ja rahdinkuljetuspalveluun. Tämän vuoksi lähetyksen rahdinkuljettaja ja rahdinkuljetuspalvelu on määritettävä ja ne on linkitettävä toimitustapaan. Toimitustapa liittyy vaarallisten aineiden määräykseen.

Seuraava kuva osoittaa, missä järjestyksessä tehtävät tapahtumat, kun järjestelmä luo vaarallisten aineiden raportin.

![Tehtävien järjestys vaarallisten aineiden raporteissa](media/hazmat-report-sequence.png "Tehtävien järjestys vaarallisten aineiden raporteissa")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Vaarallisten aineiden raportoinnin määrittäminen

Yleensä vaarallisia aineita sisältäviä nimikkeitä lähetettäessä on luotava tietyt raportit, joiden avulla voidaan varmistaa turvallisuus ja noudattaa vaarallisia aineita koskevia määräyksiä. Raportit määritetään seuraavasti:

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
2. Avaa **Raportit**-välilehti. Määritä seuraavat kentät **Vaarallisten aineiden raporttiparametri** -pikavälilehdessä.

    | Osa | Kenttä | kuvaus |
    |---|---|---|
    | Multimodaaliset vaaralliset tuotteet | Sääntelykoodi | Valitse määräys, jota käytetään **Multimodaaliset vaaralliset tavarat** -raporttia luotaessa. |
    | Vaarallisten aineiden varastointirajat | Sääntelykoodi | Valitse määräys, jota käytetään varastointirajoja arvioitaessa. |
    | Tavaran kuljetus maanteitse | CMR-ryhmän tuote | CMR-lyhenne tarkoittaa karsinogeenisia, mutageenisia ja lisääntymiselle vaarallisia aineita. Kun asetukseksi valitaan **Kyllä**, järjestelmä määritetään tulostamaan tietyt näiden aineiden käsittelyyn liittyvät varoitukset ja ilmoitukset. |
    | Tavaran kuljetus maanteitse | Vaarallisen materiaalin ryhmän kuvaus | Anna niiden varoitusten teksti, jotka liittyvät CMR-ryhmään ja tavaran kuljetukseen maanteitse. Tämä teksti sisällytetään raporttiin. |
    | Huolitsijan ilmoitus | Varoitus | Anna varoituksen teksti, joka on tulostettava huolitsijan ilmoituslomakkeeseen (esimerkiksi Varoitus: vaarallisia aineita, tulenarka). |
    | Huolitsijan ilmoitus | Alatunnisteen ilmoitus | Anna huolitsijan ilmoituksen alareunaan tulostettavan ilmoituksen teksti. |
    | Vaarallisten tuotteiden raporttikieli | Vaarallisten kotimaan tuotteiden raporttikieli | Valitse kotimaan toimituksiin liitettävien vaarallisten aineiden raporttien oletuskieli. |
    | Vaarallisten tuotteiden raporttikieli | Vaarallisten vientituotteiden raporttikieli | Valitse kansainvälisiin toimituksiin liitettävien vaarallisten aineiden raporttien oletuskieli. |

## <a name="hazardous-materials-report"></a>Vaarallisten aineiden raportti

**Vaarallisten aineiden** raportissa on luettelo kaikista nimikkeitä, jotka on määritetty sisältämään tietoja vaarallisista aineista. Tämän raportin avulla voi seurata ja tarkastella ylläpidettäviä tietoja. Raportin sivulla on osa vaarallisten aineiden määrityksessä käytettävistä kentistä. Voit kuitenkin mukauttaa raporttia ja lisätä tarvittaessa muita kenttiä.

Voit tarkastella raporttia valitsemalla **Tuotetietojen hallinta \> Kyselyt ja raportit \> Vaarallisten aineiden lähetysohjeet \> Vaaralliset aineet**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Vaarallisten aineiden varastointiraja -raportti

**Vaarallisen aineen varastoraja** -raportin avulla voi seurata vaarallisten aineiden varastotasoja varastoissa ja varmistaa, että tässä kohdassa määritettyjä turvarajoja noudatetaan. Nämä rajat saadaan rajoista, jotka on määritetty kullekin vapautetulle tuotteelle.

Voit tarkastella raporttia valitsemalla **Tuotetietojen hallinta \> Kyselyt ja raportit \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden varastointirajat**.

Lisätietoja vapautetun tuotteen varastointirajojen määrittämisestä on kohdassa [Vaarallisten tuotteiden varastointirajojen määrittäminen](hazmat-items.md#stock-limits).

Varastointirajoissa käytetty määräys määritetään **Varastonhallinnan parametrit** -sivulla. Valitse **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit** ja määritä sitten määräyksen koodi **Raportit**-välilehden **Vaarallisten aineiden varastointiraja** -kohdassa. Lisätietoja on aiemmin tässä ohjeaiheessa kohdassa [Vaarallisten aineiden raportoinnin määrittäminen](#set-up).

## <a name="verified-gross-mass-report"></a>Vahvistettu bruttopaino -raportti

**Vahvistettu bruttopaino** -raportissa voi tulostaa lähetyksen painoa koskevia tietoja.

Voit luoda ja tulostaa tämän raportin valitsemalla **Varastonhallinta \> Lähetykset \> Kaikki lähetykset** ja avaamalla lähetyksen. Valitse sitten toimintoruudun **Lähetykset**-välilehden **Vaarallisten aineiden asiakirja** -ryhmässä **Vahvistettu bruttopaino**.

## <a name="multimodal-dangerous-goods-report"></a>Multimodaaliset vaaralliset tuotteet -raportti

**Multimodaaliset vaaralliset tuotteet** -raporttia käytetään lähetyksissä, joiden siirtämiseen on käytettävä erilaisia kuljetustapoja. Sitä käytetään yleensä silloin, kun lähetys siirretään ensin maanteitse ja myöhemmin meritse.

Voit luoda ja tulostaa tämän raportin valitsemalla **Varastonhallinta \> Lähetykset \> Kaikki lähetykset** ja avaamalla lähetyksen. Valitse sitten toimintoruudun **Lähetykset**-välilehden **Vaarallisten aineiden asiakirja** -ryhmässä **Multimodaaliset vaaralliset tuotteet**.

Kun tämä raportti luodaan, tiedot tallennetaan siten, että voit muokata sitä ja/tai tulostaa raportin tarvittaessa uudelleen. Luotua raporttia voi muokata valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Vaarallisten aineiden lähetysohjeet \> Multimodaaliset vaaralliset tuotteet** ja etsimällä raportin luettelosta. Kun sisällön muokkaus on valmis, tulosta raportti valitsemalla toimintoruudussa **Tulosta**.

## <a name="shippers-declaration-report"></a>Huolitsijan ilmoitus -raportti

**Huolitsijan ilmoitus** -raportin avulla voi tulostaa tietoja, jotka liittyvät lähetykseen sisältyviä materiaaleja koskevaan ilmoitukseen.

Voit luoda ja tulostaa tämän raportin valitsemalla **Varastonhallinta \> Lähetykset \> Kaikki lähetykset** ja avaamalla lähetyksen. Valitse sitten toimintoruudun **Lähetykset**-välilehden **Vaarallisten aineiden asiakirja** -ryhmässä **Huolitsijan ilmoitus**.

## <a name="carriage-of-merchandise-by-road-report"></a>Tavaran kuljetus maanteitse -raportti

**Tavaran kuljetus maanteitse** -raportti muistuttaa rahtikirjaa, mutta sitä käytetään yleensä eurooppalaisissa maantiekuljetuksissa ADR-sopimuksen (vaarallisten aineiden kansainvälisiä tiekuljetuksia koskeva sopimus) määräysten mukaisesti. Tässä raportissa käytetään nimikkeen tulostettavaa lähetysteksti, ellei **Vaarallisten aineiden ryhmäkuvaus** -kenttää määritetä **Varastonhallinnan parametrit** -sivulla.

Voit luoda ja tulostaa tämän raportin valitsemalla **Varastonhallinta \> Lähetykset \> Kaikki lähetykset** ja avaamalla lähetyksen. Valitse sitten toimintoruudun **Lähetykset**-välilehden **Vaarallisten aineiden asiakirja** -ryhmässä **Tavaran kuljetus maanteitse**.

Kun tämä raportti luodaan, tiedot tallennetaan siten, että voit muokata sitä ja/tai tulostaa raportin tarvittaessa uudelleen. Luotua raporttia voi muokata valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Vaarallisten aineiden lähetysohjeet \> Tavaran kuljetus maanteitse** ja etsimällä raportin luettelosta. Kun sisällön muokkaus on valmis, tulosta raportti valitsemalla toimintoruudussa **Tulosta**.

## <a name="shipment-summary-report"></a>Lähetyksen yhteenvetoraportti

**Lähetyksen yhteenveto** -raportissa on tietoja, jotka liittyvät vapautettuihin nimikkeisiin ja joiden yhteenveto on tehty kuljetusluokittain.

Voit luoda ja tulostaa tämän raportin valitsemalla **Varastonhallinta \> Lähetykset \> Kaikki lähetykset** ja avaamalla lähetyksen. Valitse sitten toimintoruudun **Lähetykset**-välilehden **Vaarallisten aineiden asiakirja** -ryhmässä **Lähetyksen yhteenveto**.

## <a name="bill-of-lading-report"></a>Rahtikirjaraportti

Jos vaarallisten aineiden toiminto on otettu järjestelmässä käyttöön, **Rahtikirja**-raportti sisältää **Vaaralliset aineet** -sarakkeen, joka ilmaiseen, sisältääkö kuorma vaarallisia aineita. Tämä rapotti on saatavana tavalliseen tapaan **Kaikki kuormat** -sivulla.

## <a name="packing-list-report"></a>Pakkausluetteloraportti

Jos vaarallisten aineiden toiminto on otettu järjestelmässä käyttöön, pakkausluettelo sisältää nimikkeen tulostettavaan lähetystekstiin liittyviä tietoja. Tämä rapotti on saatavana tavalliseen tapaan **Kaikki kuormat** -sivulla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]