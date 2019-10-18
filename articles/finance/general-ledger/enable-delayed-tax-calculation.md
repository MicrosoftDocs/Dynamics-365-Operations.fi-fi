---
title: Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansiossa
description: Tässä ohjeaiheessa tapaa, jolla **Ota käyttöön viivästyneen veron laskeminen kirjauskansiossa** -toiminnolla voi tehostaa veron laskemista, kun kirjauskansiossa on erittäin suuri määrä rivejä.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177497"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansiossa
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa tapaa, jolla **Ota käyttöön viivästyneen veron laskeminen kirjauskansiossa** -toiminnolla voi tehostaa veron laskemista, kun kirjauskansiossa on erittäin suuri määrä rivejä.

Tällä hetkellä arvonlisäveron laskenta käynnistyy kirjauskansiossa, kun käyttäjä päivittää veroon liittyviä kenttiä, kuten arvonlisäveroryhmän tai nimikkeen arvonlisäveroryhmän. Aina kun kirjauskansion rivitasolla tehdään päivitys, kaikkien kirjauskansion rivien verosumma lasketaan uudelleen. Käyttäjä näkee tällä tavoin reaaliaikaisen lasketun verosumman, mutta seurauksena voi olla suorituskykyongelmia, jos kirjauskansiossa on erittäin paljon rivejä.

Tämä toiminto antaa mahdollisuuden ratkaista suorituskykyongelma viivästyttämällä veron laskentaa. Jos tämä ominaisuus on otettu käyttöön, verosumma lasketaan vain silloin, kun käyttäjä valitsee Arvonlisävero-komennon tai tekee kirjauksen kirjauskansioon.

Käyttäjä voi ottaa parametrin käyttöön tai poistaa sen käytöstä kolmella tasolla:
- Yrityskohtainen
- Kirjauskansion nimen perusteella
- Kirjauskansion otsikon perusteella

Järjestelmän pitää kirjauskansion otsikossa olevaa parametrin arvoa lopullisena. Kirjauskansion otsikon parametrin oletusarvo saadaan kirjauskansion nimestä. Kirjauskansion nimen parametrin oletusarvo saadaan kirjanpitoparametrista kirjauskansion nimen luonnin yhteydessä.

Kirjauskansion Toteutunut arvonlisäverosumma- ja Laskettu arvonlisäveron summa -kentät piilotetaan, jos tämä parametri on otettu käyttöön. Tällä tavoin voidaan estää sekaannukset, koska ennen veron laskemisen käynnistämistä näiden kahden kentän arvo on aina 0.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Yrityskohtaisen viivästyneen veron laskemisen ottaminen käyttöön

1. Valitse **Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**.
2. Valitse **Arvonlisävero**-välilehti.
3. Etsi **Yleiset**-välilehdessä parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansion nimen perusteella

1. Valitse **Kirjanpito > Kirjauskansion asetukset > Kirjauskansioiden nimet**.
2. Etsi **Yleiset**-välilehdessä parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansion perusteella

1. Valitse **Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot**.
2. Valitse **Uusi**.
3. Valitse kirjauskansion nimi.
4. Valitse **Asetukset**.
5. Etsi parametri **Viivästynyt veron laskenta** ja ota parametri käyttöön tai poista se käytöstä.

![](media/delayed-tax-calculation-journal-header.png)
