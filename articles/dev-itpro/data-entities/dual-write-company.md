---
title: Yrityksen käsite Common Data Servicessa
description: Tässä aiheessa kuvataan yrityksen tietojen intergraatiota Finance and Operationsin ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6eddd87c3ad3ea9de8aec2874b0514faa65374f1
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789184"
---
## <a name="company-concept-in-common-data-service"></a>Yrityksen käsite Common Data Servicessa

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operationsissa käsite *Yritys* on sekä oikeudellinen että liiketoiminnallinen yksikkö. Se on myös tietojen suojauksen ja näkyvyyden raja. Käyttäjät työskentelevät aina yksittäisen yrityksen kontekstissa, ja suurin osa tiedoista on yrityksen omistamia.

Common Data Servicessa ei ole vastaavaa käsitettä. Lähin käsite on *liiketoimintayksikkö*, joka on ensisijaisesti tietoturvan ja näkyvyyden raja käyttäjätiedoille. Tällä käsitteellä ei ole sama oikeudellisia tai liiketoiminnan vaikutuksia kuin yrityksen käsitteellä Finance and Operationsissa.

Koska liiketoimintayksikkö ja yritys eivät ole vastaavia käsitteitä, ei ole mahdollista pakottaa yksi-yhteen (1:1)-vastaavuutta niiden välillä Common Data Service -integrointia varten. Koska käyttäjien on kuitenkin oletusarvoisesti pystyttävä näkemään samat tietueet Finance and Operationsissa ja Common Data Servicessa, Microsoft on ottanut käyttöön uuden entiteetin Common Data Servicessa, jonka nimi on cdm\_Company. Tämä entiteetti vastaa Finance and Operationsin yritysentiteettiä. Jos haluat varmistaa, että tietueiden näkyvyys vastaa toisiaan Finance and Operationsin ja Common Data Servicen välillä heti valmiina, suosittelemme seuraavaa tietojen määritystä Common Data Servicessa:

+ Jokaiselle Finance and Operationsin Yritys-tietueelle, jolle on otettu käyttöön kaksoiskirjoitus, luodaan liittyvä cdm\_Company-tietue.
+ Kun cdm\_Company-tietue luodaan ja otetaan käyttöön kaksoiskirjoitukselle, luodaan oletusliiketoimintayksikkö, jolla on sama nimi. Vaikka kyseiselle liiketoimintayksikölle luodaan automaattisesti oletusryhmä, liiketoimintayksikköä ei käytetä.
+ Luodaan erillinen omistajaryhmä, jolla on sama nimi. Se liittyy myös liiketoimintayksikköön.
+ Oletusarvon mukaan minkä tahansa Finance and Operationsissa luodun ja Common Data Serviceen kaksoiskirjoitetun tietueen omistajaksi määritetään "DW Owner"-ryhmä, joka on linkitetty liittyvään liiketoimintayksikköön.

Seuraavassa kuvassa on esimerkki tästä tietojen määrityksestä Common Data Servicessa.

![Tietojen määritys Common Data Servicessa](media/dual-write-company-1.png)

Tämän määrityksen vuoksi kaikki USMF-yritykseen liittyvät Finance and Operations -tietueet omistaa ryhmä, joka on linkitetty USMF-liiketoimintayksikköön Common Data Servicessa. Tämän vuoksi jokainen käyttäjä, jolla on liiketoimintayksikön käyttöoikeusrooli, joka on määritetty liiketoimintayksikkötason näkyvyydelle, voi nyt nähdä kyseiset tietueet. Seuraavassa esimerkissä kerrotaan, miten ryhmiä voidaan käyttää kyseisten tietueiden oikeisiin käyttöoikeuksiin.

+ Myyntipäällikkö-rooli määritetään USMF Sales -tiimin jäsenille.
+ Käyttäjät, joilla on Myyntipäällikkö-rooli, voivat käyttää mitä tahansa tilin tietueita, jotka ovat saman liiketoiminta yksikön jäseniä.
+ USMF Sales -tiimi on linkitetty aiemmin mainittuun USMF-liiketoimintayksikköön.
+ Tämän vuoksi USMF Sales -tiimin jäsenet näkevät minkä tahansa tilin, jonka omistaa USMF DW, joka olisi tullut USMF-yrityksen entiteetistä Finance and Operationsissa.

![Miten ryhmiä voidaan käyttää](media/dual-write-company-2.png)

Kuten edellä olevassa kuvassa näkyy, tämä 1:1-yhteys liiketoimintayksikön, yrityksen ja tiimin välillä on vain lähtökohta. Tässä esimerkissä uusi Europe-liiketoimintayksikkö luodaan manuaalisesti Common Data Servicessa sekä DEMF:n että ESMF:n ylätasona. Tämä uusi pääliiketoimintayksikkö ei liity kaksoiskirjoittamiseen. Sen avulla voidaan kuitenkin antaa "EUR Sales"-tiimin jäsenille pääsy tilitietoihin sekä DEMF:ssä että ESMF:ssä asettamalla tietojen näkyvyydeksi **Ylätaso/aliliiketoimintayksikkö** liittyvässä käyttöoikeusroolissa.

Viimeinen aihe, josta keskustellaan, on se, miten kaksoiskirjoitus määrittää, mihin omistajaryhmään sen tulisi liittää tietueita. Tätä toimintaa ohjaa cdm\_Company-tietueen **Oletusomistajaryhmä**-kenttä. Kun cdm\_Company-tietueelle on otettu käyttöön kaksoiskirjoitus, laajennus luo automaattisesti liittyvän liiketoimintayksikön ja omistajaryhmän (jos sitä ei vielä ole) ja määrittää **Oletusomistajaryhmä**-kentän. Järjestelmänvalvoja voi muuttaa kentän arvoksi eri arvon. Järjestelmänvalvoja ei kuitenkaan voi tyhjentää kenttää niin kauan kuin entiteetti on kaksoiskirjoitustilassa.

![Oletusomistajaryhmä-kenttä](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Yrityksen tietojen omistajuus ja esilataus

Common Data Service -integrointi tuo yrityksen pariteetin käyttämällä yritystunnusta tietojen omistajuuden ilmaisemiseen. Kuten seuraavassa kuvassa näkyy, kaikkia yrityskohtaisia entiteettejä laajennetaan siten, että niillä on monta-yhteen (N:1)-suhde cdm\_Company-entiteetin kanssa.

![N:1-suhde yrityskohtaisen entiteetin ja cdm_Company-yksikön välillä](media/dual-write-bootstrapping.png)

+ Kun yritys on lisätty ja tallennettu, arvo tietueissa muuttuu vain luku -arvoksi. Siksi käyttäjien tulee varmistaa, että he valitsevat oikean yrityksen.
+ Vain tietueet, joissa on yritystietoja, voivat olla kaksoiskirjoituskelpoisia Finance and Operationsin ja Common Data Servicen välillä.
+ Olemassa olevien Common Data Service -tietojen osalta on pian saatavilla järjestelmänvalvojan johtama esilatauskokemus.
