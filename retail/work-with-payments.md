---
title: Puhelinkeskuksen maksutavat
description: "Tässä ohjeaiheessa käsitellään vähittäismyynnin ja kaupan puhelinkeskuksessa käytettäviä maksutapoja."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ec9bc4ff511c13740c6f63728bb3d0f837670293
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="payment-methods-in-a-call-center"></a>Puhelinkeskuksen maksutavat

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa käsitellään vähittäismyynnin ja kaupan puhelinkeskuksessa käytettäviä maksutapoja.

Puhelinkeskuksissa voidaan käyttää myös muissa Microsoft Dynamics AX:n vähittäismyynti- ja kauppakanavissa käytettyjä maksutapoja, kuten käteinen, sekki, luottokortit ja lahjakortit. Kun olet määrittänyt puhelinkeskuksen maksutavan, se näkyy vaihtoehtona puhelinkeskuksen käyttäjille **Myyntitilaus**-sivun **Maksut**-osassa. Voit lisäksi määrittää kuponkeja tarjotaksesi asiakkaille alennuksia, kun he tekevät tilauksen yrityksen puhelinkeskukseen. Kupongit voivat määrittää kiinteän määräalennuksen tai prosenttimäärän nimikehinnasta tai tilauksen kokonaissummasta. Esimerkiksi summaperusteinen kuponki voi antaa asiakkaille 75,00:n alennuksen, kun asiakas käyttää 750,00 tai enemmän. Voit luoda erilaisia kuponkeja, määrittää pää-ja alikuponkeja sekä kopioida tai mitätöidä kupongin. Luo kuponkeja seuraavan taulukon vaihtoehdoilla.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Määrite**             | Anna **Lunastusprosentti**-kenttään kupongin odotettu lunastushinta prosenttiosuutena ja valitse, käytetäänkö kuponkia kertaalleen, myönnetäänkö se automaattisesti uudelleen vai onko se asiakaskohtainen.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Kelvollinen**                 | Anna **Alkamispäivä**- ja **Päättymispäivä**-kenttään ensimmäinen ja viimeinen päivämäärä, jolloin kuponki on voimassa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Sisällytä säännöt tai jätä säännöt pois** | Valitse **Luettelot**- ja **Nimikkeet**-kentissä, sisältyvätkö luettelot tai nimikkeet kuponkiin vai jätetäänkö ne pois kupongista. Jos valitset **Sisällytä** tai **Jätä pois**, valitse ensin **Määritä**, sitten **Sisällytä luettelot tai jätä luettelot pois** tai **Sisällytä tuotteet tai jätä tuotteet pois** ja anna luetteloa tai nimikettä koskevat tiedot. Jos valitset näissä kentissä **Ei mitään**, kaikki luettelot tai nimikkeet jätetään pois kupongista.                                                                                                                                                                                                                          |
| **Muut**         | Jos kuponkia ei voi käyttää yhdessä muiden alennusten kanssa, valitse **Jätä pois** -valintaruutu. Valitse sitten **Peruste**-kentässä, missä kuponkia käytetään. Jos kyseessä on valmistajan kuponki, valitse **Valmistajan kuponki** -valintaruutu.                                                                                                                                                                                                                                                                                                                                                                |
| **Tuleva kuponki**         | Jos tämä kuponki liitetään muiden kuponkeihin pääkuponkina, valitse **Pääkuponki**-valintaruutu. Jos tämä kuponki on liitettävä aiemmin luotuun kuponkiin alikuponkina, valitse pääkuponki **Pääkupongin tunnus** -kentässä. Voit luoda esimerkiksi kupongin tulevaan kevätkuvastoon. Kaikki muut kevätkuvastoa varten luomasi kupongit ovat kevätkuvastokupongin alikuponkeja. Alikupongit voivat sisältää 20 prosentin alennuksen uusille asiakkaille, 10 prosentin alennuksen äskettäin julkaistuille nimikkeille tai 95,00:n alennuksen, jos tilaus on vähintään 1 000,00. |

Jos lähetät luottokorttimaksun **Myyntitilaus**-sivulta ja avautuva ilmoittaa, että korttia ei vielä ole hyväksytty, voit käsitellä valtuutuksen manuaalisesti. Voit hyväksyä, hylätä tai lähettää luottokorttitapahtuman uudelleen **Valtuutuksenhallinta**-sivulla. Voit määrittää maksun käsittelyn lisäasetuksia puhelinkeskuksen parametrisivulla:

-   Sekkipidoilla taloushallinnon henkilöstä voi käsitellä tilauksia, jotka on asetettu pitoon, koska maksutapana on käytetty sekkiä ja sekkipidon rajasumma on ylitetty. Pito voidaan vapauttaa manuaalisesti, tai se vanhenee automaattisesti määritetyn kauden lopussa.
-   Voit määrittää raja-arvot, joita ylittäessä sekkien ja luottokorttien kautta annettavat palautukset on hyväksyttävä manuaalisesti. Kynnyssumman ylittävät palautukset lisätään hyväksyntäjonoon. Kun palautus on hyväksytty, palautusmyyntitilaus voidaan laskuttaa.





