---
title: Ylläpitoaikataulun kustannus
description: Tässä ohjeaiheessa kerrotaan ylläpitoaikataulun kustannuksista resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9cbb1d81f9108a908bdfdd2a27b92b685d3afdac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361015"
---
# <a name="maintenance-schedule-cost"></a>Ylläpitoaikataulun kustannus

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuuden hallinnassa voit laskea ylläpitoaikataulurivien budjetoidut kustannukset. Tästä on hyötyä, jos haluat saada yleiskuvan odotetuista kustannuksista, esimerkiksi kustannukset, jotka liittyvät suunniteltuihin ennaltaehkäiseviin kunnossapitotöihin ensi vuodelle. Laskelmat perustuvat olemassa oleviin ylläpitoaikatauluriveihin, joiden tyyppi on "huoltosuunnitelmat" ja "ylläpitokierrokset" ja "ylläpitopyynnöt".

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Ylläpitoaikataulun kustannus**.

2. **Ylläpitoaikataulun kustannus** -valintaikkunassa voit valita **Taloushallinnon dimensioyhdistelmä** -kohdan, jos haluat tarkastella taloushallinnon dimensioihin ryhmiteltyjä kustannuksia.

>[!NOTE]
>Taloushallinnon dimensioyhdistelmät määritetään kohdassa **Kirjanpito** > **Tilikartta** > **Dimensiot** > **Taloushallinnon dimensioyhdistelmät.**

3. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoaikataulun riveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitoaikataulun rivit työtilaukset näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitoaikataulun rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

4. Jos haluat määrittää tiettyjen resurssien laskennat, valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodata** ja valitse sitten haluamasi käyttöomaisuudet. Tarvittaessa voit myös määrittää kustannuslaskennalle **Odotettu alkamispäivämäärä** -kentän tai valita kustannuslaskennalle toisen **Tila**-kentän arvon.

5. Aloita ksustannuslaskenta valitsemalla **OK**.

6. Valitse **Ylläpitoaikataulun kustannus** -välilehden toimintoruudun **Ryhmittely...**-ryhmissä painikkeet, joilla saadaan näkyviin tarvittava kustannuslaskennan erittelytaso. Valitut toimintoruuturyhmän painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

7. Valitse **Laske kustannus** -painike, jos haluat tehdä uuden kustannuslaskennan.

Alla oleva kuva näyttää ylläpitoaikataulun kustannusten laskemisen tulokset.

![Kuva 1.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]