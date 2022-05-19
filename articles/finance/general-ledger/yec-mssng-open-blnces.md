---
title: Alkusaldot puuttuvat tilinpäätöksestä
description: Tässä ohjeaiheessa kerrotaan, miksi alkusaldot saattavat puuttua tilinpäätöksen yhteydessä, ja miten nämä puuttuvat saldot muodostetaan uudelleen.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 582363ba6c5f6e63e695d41e73ee2f0b382cf26e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727169"
---
# <a name="year-end-close-missing-opening-balances"></a>Alkusaldot puuttuvat tilinpäätöksestä

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miksi alkusaldot saattavat puuttua tilinpäätöksen yhteydessä, ja miten nämä puuttuvat saldot muodostetaan uudelleen.

### <a name="symptom"></a>Oire

Miksi alkusaldoja ei ole kirjanpidon tilinpäätöksen suorittamisen jälkeen? 

### <a name="resolution"></a>Ratkaisu

Tarkista alla olevat kohdat, jos kirjanpidon tilinpäätös on tehty ja tämän jälkeen luotu pääkirja, jossa eivät näy seuraavan tilikauden alkusaldot.

Jos **Kumoa edellinen sulkeminen** ‑kentän arvoksi on valittu **Kyllä**, edellinen saman tilikauden tilinpäätös peruutetaan. Kun suoritetaan prosessi, joka peruuttaa tilinpäätöksen, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettu. Tositteet poistetaan myös. Tilinpäätösprosessia ei suoriteta uudelleen automaattisesti. Prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi päivitetään **Ei**.

Tämä skenaario sisältyy aiheeseen, jossa käsitellään tilinpäätöstä koskevia usein kysyttyjä kysymyksiä. Lisätietoja on kohdassa [Vuoden lopun toimintoja koskevat usein kysytyt kysymykset](faq-year-end-activities.md).

### <a name="symptom"></a>Oire

Suoritin tilinpäätöksen niin, että **Kumoa edellinen sulkeminen** -asetuksen arvo oli **Ei**. Tästä huolimatta tilikausi ei sisällä alkusaldoja.

### <a name="resolution"></a>Ratkaisu

Tarkista ensin erätyön tila. Tilinpäätös sisältää useita yksittäisiä tehtäviä. Kriittisin tehtävä on erätehtävä, jonka tehtävän kuvaus on **Vaihe 5.0.0**. Avaustapahtumien tai vaihtoehtoisesti päätöstapahtumien kirjaaminen kirjanpitoon tapahtuu tämän vaiheen aikana. 

[![Erätyöhistorialuettelo.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Jos tämän vaiheen suorittaminen onnistuu, mutta alkusaldot eivät näy **Pääkirjan kysely** -sivulla (**Kirjanpito > Kyselyt ja raportit > Pääkirja**), tarkista tilinpäätöksen erätyön tuloksista, onnistuiko Muodosta saldot uudelleen -vaiheen suorittaminen.

[![Tilinpäätöksen erätyön tulokset.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Jos tämä vaihe on epäonnistunut jonkin syyn vuoksi, alkutapahtumien (tai vaihtoehtoisesti päättämistapahtumien) kirjaaminen todennäköisesti onnistui. Tarkista, että kirjanpidon tapahtumien kirjaaminen onnistui, käyttämällä **Tositetapahtumien kysely** -sivua. Sivulla määritetään tositteen numero ja kyseisen vuoden tilinpäätösvalintaikkunassa oleva päivämäärä (**Kirjanpito > Kyselyt ja raportit > Tositetapahtumat**).

[![Tositetapahtumien kysely.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Jos avaustapahtumien (tai vaihtoehtoisesti päätöstapahtumien) tositteet ovat näkyvissä, tilinpäätöstä ei tarvitse suorittaa uudelleen. Katso sen sijaan seuraavan osan ohjeita seuraavien toimintojen suorittamiseksi.

### <a name="symptom"></a>Oire

Tilinpäätöksen Muodosta saldot uudelleen -vaihe epäonnistui. Tuleeko minun suorittaa koko tilinpäätösprosessi uudelleen?

### <a name="resolution"></a>Ratkaisu

Muodosta saldot uudelleen -vaihe päivittää kirjanpidon saldot, joita käytetään pääkirjan kyselyn luomisen yhteydessä.  Se on tilinpäätösprosessin viimeinen vaihe.  Jos tämä on ainoa epäonnistunut vaihe, kirjanpitotapahtumat on kirjattu onnistuneesti.  Tilinpäätöstä ei tarvitse suorittaa uudelleen. Voit suorittaa saldojen uudelleenmuodostusprosessin manuaalisesti **Taloushallinnon dimensioyhdistelmät** -sivulla (**Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensioyhdistelmät**).

[![Muodosta saldot uudelleen -painike Taloushallinnon dimensioyhdistelmät -sivulla.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Jos tämän vaiheen käsittely kestää kauan, suosittelemme taloushallinnon dimensioyhdistelmien parhaiden käytäntöjen tarkastelemista kohdassa [Taloushallinnon dimensioyhdistelmien päivittämisen parhaat käytännöt](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

