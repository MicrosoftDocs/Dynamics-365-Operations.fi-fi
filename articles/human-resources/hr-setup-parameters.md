---
title: Määritä henkilöstöparametreja
description: Jotkin henkilöstöhallinnon parametrien asetukset ovat yhteisiä eri yrityksissä, toiset taas yrityskohtaisia. Tässä artikkelissa on selostettu, miten määritetään yrityskohtaisia henkilöstöhallinnon parametreja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25ef0b515e455be7493ac816f9c5e0db08dfd483
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008911"
---
# <a name="configure-human-resources-parameters"></a>Määritä henkilöstöparametreja

Jotkin henkilöstöhallinnon (HR) parametrien asetukset ovat yhteisiä eri yrityksissä, toiset taas yrityskohtaisia. Tässä artikkelissa on selostettu, miten määritetään yrityskohtaisia henkilöstöhallinnon parametreja.

Henkilöstöhallinto (HR)-parametrien määrittämiseen käytetään kahta sivua. Käytä yhtiöiden kesken jaettujen parametrien määrittämiseen **Henkilöstöhallinnon jaetut parametrit** -sivua. Käytä yhtiökohtaisten (ts. asetukset koskevat yhtä yhtiötä) parametrien määrittämiseen **Henkilöstöparametrit**-sivua. **Henkilöstöparametrit**-sivulla asetukset jaetaan kuudelle välilehdelle:

-   Yleiset
-   Työhönotto – ei sisälly Dynamics 365 Human Resourcesiin
-   Kompensaatio
-   Numerosarjat
-   Perhe ja sairauspoissaolon säädös (FMLA)
-   Työntekijän itsepalvelu

Kukin välilehti sisältää yksittäistä yhtiötä koskevia tietoja. **Yleinen**-välilehdellä määritetään poissaoloja, tapaturmia ja sairaustapauksia sekä uusia työntekijöitä koskevien tietojen ulkonäkö. Tämän välilehden asetukset määrittävät myös osan oletusarvoista, jotka tulevat näkyviin työskentelysi aikana. Tarkemmin sanoen, tällä välilehdellä voit valita avoimissa poissaolotapahtumissa käytettävän värin, määrittää raporteissa käytettävän tyylitiedoston, määrittää, otetaanko integrointi käyttöön koulutusten ja poissaolomerkintöjen välillä, ja valita tämän integroinnin hallinnassa käytettävä poissaolokoodi. Voit myös määrittää, miten pitkään loukkaantumis- ja sairaustapauksia säilytetään, ja määrittää oletusarvoisen tunnusnumeron, joka näytetään, kun uusi työntekijä palkataan. 

**Työhönotto**-välilehden asetuksilla määritetään tiedostotyypit, joita käytetään automaattisessa hakijoiden kanssa käytävässä yhteydenpidossa sekä avoimissa hakemuksissa (hakemuksissa, jotka eivät koske määrättyä työhönottoprojektia) käytettävän työhönottoprojekti. Työhönottoprosessin vanhentumisasetuksissa määritetty ajanjakso määrittää ne työhönottoprojektit, jotka sisällytetään **Vanhentuvat projektit** -ruudulle **Työhönoton hallinta** -työtilassa. Hakemuksen määräajan varoitukselle määritettyä ajanjaksoa käytetään näyttämään ne työhönottoprojektit, jotka lähestyvät hakemuksille asetettua määräaikaansa **Hakemuksen määräaika lähestyy** -ruudulla **Työhönotto**-työtilassa. 

**Kompensaatio**-välilehden asetukset määrittävät, onko käyttäjien vahvistettava, että he haluavat tallentaa joko kiinteän tai muuttuvan kompensaatiosuunnitelman asetukset. Jos valitset **Otetaan vahvistuksen tallennus käyttöön** -asetuksen, aina kun käyttäjä sulkee kompensaatioon liittyvän sivun, tälle lähetetään viesti, jossa tätä pyydetään tallentamaan tietue. Jotkin kompensaationhallinnan sivut eivät salli käyttäjille tietojen poistamista. Näin ollen, kehottamalla käyttäjiä vahvistamaan, että he haluavat tallentaa tiedot, saatat pystyä rajoittamaan tietojen määrää, jotka on tallennettu mutta joita ei voida poistaa myöhemmin. Jos **Otetaan vahvistuksen tallennus käyttöön** -valintaruutu tyhjennetään, tietueet tallennetaan aina heti, mahdollisesti jo ennen kuin käyttäjä on valmis. Jos käytät suorituskyvyn hallintaa, **Kompensaatio** -välilehdellä voit myös valita suorituskykyä arvioitaessa käytettävän arviointimallin kompensaatiosuunnitelmille määritetyn mallin asemesta. 

### <a name="previously-released-functionality"></a>Aiemmin julkaistu toiminto

**Numerojärjestys**-välilehden asetukset määrittävät numerosarjat, joita käytetään tunnusten määrittämiseen automaattisesti nimikkeille henkilöstöhallinnossa, kuten sovelluksille, poissaolomerkinnöille, kompensaatioprosessin tuloksille, tapausnumeroille, kursseille ja kurssien työjärjestyksille. Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua (valitse **Organisaation hallinto** &gt; **Numerojärjestykset** &gt; **Numerojärjestykset**).

> [!NOTE]
> Tehtyjen työtuntien määrä ei voi ylittää 1 250 tuntia, ja työsuhteen pituus ei voi ylittää 12 kuukautta. Nämä enimmäisarvot ovat Yhdysvaltojen liittovaltion lainsäädännön mukaiset. Lopuksi, **Työntekijän itsepalvelu** -välilehden asetuksissa määritellään tiedot, jotka esimiehet voivat syöttää työntekijöidensä puolesta.
