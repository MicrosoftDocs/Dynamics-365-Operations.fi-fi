---
title: Puhelinkeskuksen maksutavat
description: "Tässä ohjeaiheessa käsitellään Dynamics 365 for Retailin puhelinkeskuksessa käytettäviä maksutapoja."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 07cb1bcb3870b96e34f7f6725fe5b7da32628fde
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Puhelinkeskuksen maksutavat
<a id="payment-methods-in-a-call-center" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa käsitellään Dynamics 365 for Retailin puhelinkeskuksessa käytettäviä maksutapoja.

Puhelinkeskuksissa voidaan käyttää myös muissa kanavissa käytettyjä maksutapoja, kuten käteinen, sekki, luottokortit ja lahjakortit. Kun olet määrittänyt puhelinkeskuksen maksutavan, se näkyy vaihtoehtona puhelinkeskuksen käyttäjille **Myyntitilaus**-sivun **Maksut**-osassa. Voit lisäksi määrittää kuponkeja tarjotaksesi asiakkaille alennuksia, kun he tekevät tilauksen yrityksen puhelinkeskukseen. Kupongit voivat määrittää kiinteän määräalennuksen tai prosenttimäärän nimikehinnasta tai tilauksen kokonaissummasta. Esimerkiksi summaperusteinen kuponki voi antaa asiakkaille 75,00:n alennuksen, kun asiakas käyttää 750,00 tai enemmän. Voit luoda erilaisia kuponkeja, määrittää pää-ja alikuponkeja sekä kopioida tai mitätöidä kupongin. Luo kuponkeja seuraavan taulukon vaihtoehdoilla.

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





