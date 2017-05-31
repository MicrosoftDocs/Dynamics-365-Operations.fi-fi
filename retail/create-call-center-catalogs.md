---
title: Puhelinkeskuksen luettelon luominen
description: "Tämä artikkeli sisältää yleiskuvauksen puhelinpalvelukeskuksen luettelon luontiprosessista."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ef58d4b2028aee5bccd9f060abed8342381888eb
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-call-center-catalog"></a>Puhelinkeskuksen luettelon luominen

[!include[banner](includes/banner.md)]


Tämä artikkeli sisältää yleiskuvauksen puhelinpalvelukeskuksen luettelon luontiprosessista. 

Puhelinkeskuksessa voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota asiakkaille. Puhelinkeskukset käyttävät yleensä tulostettuja luetteloita. Tulostetun luettelon suunnittelu ja tuotanto käsitellään Microsoft Dynamics 365 for Operationsin ulkopuolella. Voit kuitenkin luoda ja tallentaa luettelon digitaalisessa muodossa Dynamics 365 for Operationsin Vähittäismyynti ja kauppa -osiossa käyttämällä samoja lomakkeita, joita käytät verkkoluetteloiden määrittämiseen. Ennen kuin voit luoda luettelon, sinun on asetettava tuotevalikoimat ja määritettävä valikoimat puhelinkeskukselle. Lisäät sitten tuotteet luetteloon valitsemalla tuotteet näistä valikoimista. Kun tuotteet on lisätty luetteloon ja luettelo on valmis, sen tiedot on varmennettava. Tämän jälkeen sinun on lähetettävä luettelo arvioitaviksi ja hyväksyttäviksi. Kun luettelo on hyväksytty, se voidaan julkaista. Kun puhelinkeskuksen luettelo luodaan, voit ottaa tilannevedoksen luettelon tiedoista luettelon julkaisuhetkellä. Tilannevedostoiminto mahdollistaa tietyn luetteloversion käyttämisen, vaikka luetteloa muutetaan ja päivitetään myöhemmin. Puhelinkeskuksen luettelot voidaan määrittää myös sisältämään seuraavat valinnaiset toiminnot.

-   **Lähdekoodit** – koodit, joiden avulla seurataan asiakkaan vastausta tiettyihin luettelon postituksiin.
-   **Ilmaiset tuotteet** – tuotteet, jotka sisältyvät ilman lisämaksua asiakkaan tilaukseen. Nämä tuotteet lisätään tilaukseen automaattisesti, kun luettelon lähdekoodi kirjoitetaan tilaukseen.
-   **Komentosarjat** – tekstit, joita soittokeskuksen työntekijä lukee asiakkaalle, kun myyntitilaus luodaan. Komentosarjat voivat sisältää tervehdyksiä tai ostoehdotuksia.
-   **Lisämyynti- tai oheismyyntinimikkeet** -nimikkeet, jotka näkyvät ehdotuksina, kun tilaukseen lisätään tietty tuote.

Nämä asetukset on määritettävä ennen luettelon hyväksymistä ja julkaisemista.

## <a name="prerequisites"></a>Edellytykset
Seuraavat tehtävät on suoritettava ennen aloittamista:

-   Määritä tuotteet ja tuotevalikoimat.
-   Aseta vähittäismyyntituotteet.
-   Määritä valikoima.
-   Luo puhelinkeskus.
-   Aseta puhelinkeskus.
-   Lisää puhelinkeskus organisaatiohierarkiaan.
-   Luo organisaatiohierarkia tai muokkaa sitä.

## <a name="create-a-catalog"></a>Luo luettelo
Sinun on ensin luotava luettelo, lisättävä tuotteet luetteloon ja tarkastettava ja päivitettävä sitten tuotteiden määritteet.

## <a name="validate-the-catalog"></a>Luettelon vahvistaminen
Kun olet saanut luettelon määritettyä, se täytyy vahvistaa. Vahvistusprosessi tarkistaa, että kanavamääritteiden ja tuotemääritteiden vaatimat tiedot ovat täydellisiä ja kelvollisia ja että luettelo voidaan julkaista.

## <a name="submit-the-catalog-for-review-and-approval"></a>Luettelon lähettäminen tarkistettavaksi ja hyväksyttäväksi
Kun luettelo on vahvistettu, voit lähettää sen arvioitavaksi ja hyväksyttäväksi. Luettelo on hyväksyttävä ennen kuin se voidaan julkaista. Voit määrittää työnkulun niin, että luettelot hyväksytään automaattisesti tai edellyttävät manuaalista hyväksyntää.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Valinnainen: Lisää lähdekoodit, ilmaiset tuotteet ja käsikirjoitukset
Voit lisätä puhelinkeskuksen luetteloon myös seuraavat nimikkeet. Ne ovat valinnaisia.

-   **Lähdekoodien** avulla painettuja luetteloita käyttävät yritykset voivat seurata asiakasvasteita tiettyihin luetteloihin. Lähdekoodit tulostetaan usein luettelon taakse ja ne kirjoitetaan myyntitilaukseen, kun asiakas suorittaa oston. Jos haluat lisätä luetteloon lähdekoodia, sinun on ensin luotava kohdemarkkina. Kohdemarkkina on yleensä yhdistetty itse omistettuun tai vuokrattuun postituslistaan.
-   **Ilmaiset tuotteet** ovat kampanjanimikkeitä, jotka sisällytetään asiakkaan tilaukseen ilmaiseksi, kun luetteloon viitataan.
-   **Komentosarjoilla** voidaan ohjata työntekijän vuorovaikutusta asiakkaiden kanssa luettelon tai sen sisältämän tuotteen yhteydessä.

## <a name="publish-the-catalog"></a>Luettelon julkaiseminen
Julkaisemalla puhelinkeskusluettelon viimeistelet tuotetiedot luettelossa. Julkaiseminen ilmaisee myös, että luettelo on valmis lisätoimille, joita haluat suorittaa. Voit esimerkiksi luoda tulostetun luettelon. Voit julkaista omia luetteloita manuaalisesti, tai eräprosessin avulla voit julkaista aikataulun perusteella. Ennen kuin voit julkaista luettelon, luettelon täytyy olla vahvistettu ja hyväksytty. Jos haluat muuttaa luetteloa sen jälkeen, kun se on julkaistu, peru luettelo ja julkaise se uudelleen.




