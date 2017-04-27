---
title: "Viimeksi lisätyt tehtävien tallennustoiminnon muokkaustoiminnot"
description: "Jos tehtävien tallennustoimintoa käytetään tehtävien ohjausten luomiseen, tiedostoja voi muokata tehokkaammin tässä wikissä kuvattujen toimintojen avulla."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Viimeksi lisätyt tehtävien tallennustoiminnon muokkaustoiminnot

Jos tehtävien tallennustoimintoa käytetään tehtävien ohjausten luomiseen, tiedostoja voi muokata tehokkaammin tässä wikissä kuvattujen toimintojen avulla.

Nämä toiminnot ovat käytettävissä **Asetukset &gt; Tehtävien tallennustoiminto &gt; Muokkaa tallennetta** -valikossa.

-   Lisää vaiheita ilman, että koko tiedosto on tallennettava uudelleen.
-   Siirrä alitehtävän vaiheita ilman, että koko tiedosto on tallennettava uudelleen.
-   Tallenteen nimi- ja kuvauskenttien tiivistäminen

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Lisää vaiheita ilman, että koko tiedosto on tallennettava uudelleen
Voit nyt lisätä vaiheen tehtävän ohjauksen missä tahansa vaiheessa ilman tallenteen toistamista tai koko tiedoston tallentamista uudelleen.

1.  Valitse vaihe, joka jälkeiseen kohtaan uusi vaihe lisätään. Varmista, että vaihe on korostettu.

Tehtävien tallennustoiminto voi lisätä vaiheen vain, jos avoinna on oikea sivu. Oikea sivu on sivu, jolla uusi vaihe suoritetaan. Tehtävien tallennustoiminto määrittää aktiivisen sivun ja poistaa toiminnot käytöstä, jos avoinna ei ole oikea sivu. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Kun olet oikealla sivulla, **Lisää vaihe** -kohta on käytettävissä.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Valitse **Lisää vaihe**.

Kun valitset **Lisää vaihe**, tehtävien tallennustoiminnon tilaksi vaihdetaan tallennustila. Kaikki käyttöliittymätoiminnot tallennetaan ja lisätään käytönaikaisina vaiheina.

3. Valitse **Pysäytä**.

Voit toistaa prosessin ja lisätä haluamasi määrän vaiheita tai siirtää tarvittavan määrän alitehtäviä (seuraavassa on lisätietoja alitehtävistä).

4. Kun tehtävän ohjauksen muokkaaminen on tehty, valitse **Muokkaus valmis**. Tämän jälkeen voit tallentaa tai julkaista tehtävän ohjauksen.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Siirrä alitehtävän vaiheita ilman, että koko tiedosto on tallennettava uudelleen.
Voit siirtää alitehtävän vaiheita ilman toistoa tai koko tiedoston tallentamista uudelleen. Voit myös siirtää alitehtävän vaiheen tai lopetuksen alitehtävän vaiheen, jos haluat ryhmitellä aiemmin luotujen vaiheiden lohkon.

1.  Valitse siirrettävä vaihe tai alitehtävän vaihe. Varmista, että vaihe on korostettu.
2.  Valitse ellipsi ja valitse sitten **Siirrä vaihe seuraavan jälkeen**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Valitse siirrettävä vaihe tai alitehtävän vaihe, jonka jälkeiseen kohtaan vaihe tai alivaihe siirretään. Tehtävien tallennustoiminto siirtää vaiheen.

4. Voit siirtää lopetuksen alitehtävän vaiheen, kun valitset vaiheen ja valitset sitten ellipsin. Valitse **Siirrä vaihe seuraavan jälkeen** ja valitse sitten vaihe, jonka jälkeiseen kohtaa lopetuksen alitehtävän vaihe sijoitetaan.

Jos haluat, että tehtävän ohjauksen ensimmäinen vaihe kuuluu alitehtävään, luo alitehtävän vaiheet toisena vaiheena ja siirrä tähän ensimmäinen vaihe. Voit lisätä tai siirtää haluamasi määrän vaiheita tai alitehtäviä.

5. Kun tehtävän ohjauksen muokkaaminen on tehty, valitse **Muokkaus valmis**. Tämän jälkeen voit tallentaa tai julkaista tehtävän ohjauksen.

## <a name="collapse-recording-name-and-description"></a>Tallenteen nimen ja kuvauksen tiivistäminen
Voit laajentaa ja tiivistää **Tallenteen nimi**- ja **Tallenteen kuvaus** -kentän. Kun nämä kentät on tiivistetty, tehtävien tallennustoiminnon muokkausruudussa näkyy enemmän vaiheita. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Lisätietoja
--------

[Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Tehtävien tallennustoiminnon pikaopas](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


